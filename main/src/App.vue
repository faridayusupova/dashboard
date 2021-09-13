<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
      <router-link to="/dashboard">Dashboard</router-link>
      <router-link to="/bitcoin-details">Bitcoin Details</router-link>
      <router-link to="/bitcoin-umrechner">Bitcoin Umrechner</router-link>
      <router-link to="/bitcoin-diagram">Bitcoin Diagram</router-link>
      <router-link to="/bitcoin-umrechner">Bitcoin Umrechner</router-link>
      <router-link to="/meine-bitcoin">Meine Bitcoin</router-link>
    </div>
    <router-view />
  </div>
</template>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
