<template>
<v-container
>
<h1>Dashboard</h1>
    <v-row>
      <v-col
        v-for="ticker in tickers"
        :key="ticker.url"
        class="d-flex child-flex"
        cols="2"
      >
      {{ ticker.symbol }}
      {{ ticker.price_24h }}
      {{ ticker.volume_24h }}
      {{ ticker.last_trade_price }}
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import axios from 'axios';
export default {
  name: "Dashboard",

  data () {
    return {
      tickers: [],
    };
  },

created() {
  axios.get('https://api.blockchain.com/v3/exchange/tickers')
.then(res => {
      this.tickers = res.data;
    })
    .catch(error => {
      console.error(error);
    });
}
  
};
</script>

<style scoped>
h1 {
margin: 20px 0 20px 0;
text-decoration: underline;
text-decoration-color: red;
}
</style>
