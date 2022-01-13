<template>
  <div id="app">
    <HeroText />
    <ProjectsContainer />    
  </div>
</template>

<script>
import HeroText from "./components/HeroText.vue";
import ProjectsContainer from "./components/ProjectsContainer.vue";

export default {
  name: 'App',
  components: {
    HeroText,
    ProjectsContainer
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@200;400&display=swap');

html, body {
  margin: 0;
  background-color: #191919;
}

* {
  box-sizing: border-box;
}

#app {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: #191919;

  font-family: 'Raleway', sans-serif;  
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-weight: 400;
  overflow-y: auto;
}
</style>
