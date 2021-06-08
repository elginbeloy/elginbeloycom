<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@100;300&display=swap');

html, body {
  margin: 0;
  background-color: #191919;
}

* {
  box-sizing: border-box;
}

#app {
  font-family: 'Raleway', sans-serif;  
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-weight: 300;
}
</style>
