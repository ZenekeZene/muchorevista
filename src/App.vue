<template>
  <div id="app">
    <router-view/>
    <p>Se que tienes ganas.
    <br/>Nosotros también.
    <br/>Para Mayo lo sacamos.
    <br/>Prometido.🤞
    </p>
  </div>
</template>

<style lang="scss">
body {
  background-color: #1e1e1c;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
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
