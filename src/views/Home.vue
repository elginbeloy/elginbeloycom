<template>
  <div class="home">

    <HeroText />
    <ProjectsContainer />

  </div>
</template>

<script>

import HeroText from "@/components/HeroText.vue";
import ProjectsContainer from "@/components/ProjectsContainer.vue";

export default {
  name: 'Home',
  components: {
    HeroText,
    ProjectsContainer
  }
}

</script>

<style scoped lang="scss">

.home {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: #191919;

  overflow-y: auto;
}

@media (max-width: 800px) {
  .home {
    padding: 20px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-content: center;
  }
}
</style>