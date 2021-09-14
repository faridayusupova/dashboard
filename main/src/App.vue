<template>
  <div id="app">
    <div id="nav">
        <v-card class="overflow-hidden">
          <v-app-bar
          color="#6A76AB"
          dark
          shrink-on-scroll
          prominent
          src="https://picsum.photos/1920/1080?random"
          fade-img-on-scroll
          scroll-target="#scrolling-techniques-3"
        >
            <template v-slot:extension>
              <v-tabs align-with-title>
                <v-tab><router-link to="/dashboard">DASHBOARD</router-link></v-tab>
                <v-tab><router-link to="/bitcoin-details">BITCOIN DETAILS</router-link></v-tab>
                <v-tab><router-link to="/bitcoin-umrechner">BITCOIN UMRECHNER</router-link></v-tab>
                <v-tab><router-link to="/bitcoin-diagram">BITCOIN DIAGRAMM</router-link></v-tab>
                <v-tab><router-link to="/meine-bitcoin">MEINE BITCOIN </router-link></v-tab>
              </v-tabs>
            </template>
          </v-app-bar>
        </v-card>
    </div>
    <router-view />
  </div>
</template>

<script>

</script>


<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}

#nav {
  a {
    font-size: 24px;
        text-align: left;

    color: white;
    margin: 0px 20px 0 20px;
    text-decoration-line: none;

    &.router-link-exact-active {
      font-weight: bold;
    }
  }
  
}
</style>
