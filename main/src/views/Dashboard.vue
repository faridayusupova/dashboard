<template>
<v-container
>
<h1>Dashboard</h1>
    <v-row v-row justify="space-around">
      <v-col
        v-for="ticker in tickers"
        :key="ticker.url"
        class="d-flex child-flex"
        cols="3"
      >
      <v-card
      elevation="3"
      class="mx-auto"
      height="200px">
        <v-card-title>
          {{ ticker.symbol }}    
        </v-card-title>
        <v-spacer></v-spacer>
        <tbody>
        <tr>
          <td>Letzte 15 Minuten</td>
          <td>{{ ticker.price_24h }}</td>
        </tr>
        <tr>
          <td>Aktuell</td>
          <td>{{ ticker.price_24h }}</td>
        </tr>
        <tr>
          <td>Kaufpreis</td>
          <td>{{ ticker.price_24h }}</td>
        </tr>
        <tr>
          <td>Veraufpreis</td>
          <td>{{ ticker.price_24h }}</td>
        </tr>
      </tbody>
      </v-card>
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
th, td {
  text-align: left;
  padding: 0 0 5px 15px;
}
</style>
