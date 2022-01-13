<template>
  <div class="hero-text">
    <a class="title">
      Hey, I'm <span class="green-text">Elgin</span>
    </a>
    <a class="subtitle">
      I'm a software engineer with a wide array of passions including 
      <span class="green-text">web dev</span>,
      <span class="green-text">app dev</span>,
      <span class="green-text">game dev</span>,
      <span class="green-text">data science</span>,
      <span class="green-text">penetration testing</span>, and
      <span class="green-text">UI/UX design</span>.
    </a>
    <div class="hero-links">
      <div class="hero-links__link" @click="github">
        <img src="@/assets/github.svg" />
      </div>
      <div class="hero-links__link" @click="linkedin">
        <img src="@/assets/linkedin.svg" />
      </div>
      <div class="hero-links__link" @click="email">
        <img src="@/assets/mail.svg" />
      </div>
      <div class="hero-links__link" @click="resume">
        <img src="@/assets/resume.svg" />
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'HeroText',
  methods: {
    github: function () {   
      window.open("https://github.com/elginbeloy", "_blank");    
    },
    linkedin: function () {   
      window.open("https://www.linkedin.com/in/elgin-beloy/", "_blank");    
    },
    email: function () {   
      window.open("mailto:beloy.elgin@gmail.com", "_blank");    
    },
    resume: function () {   
      window.open(require('@/assets/resume.pdf'), "_blank");    
    },
  }
}

</script>

<style scoped>

.hero-text {
  position: -webkit-sticky;
  position: sticky;
  z-index: 100;
  top: 0%;
  left: 0%;
  height: 100%;
  width: 50%;
  padding: 100px;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}

.green-text {
  color: #2ce692;
}

.title {
  position: relative;
  width: 100%;

  color: #0071de;
  font-size: 82px;
  font-weight: 200;
  letter-spacing: 8px;
  margin-bottom: 20px;
}

.subtitle {
  position: relative;
  width: 100%;
  max-width: 800px;

  color: #0071de;
  font-size: 20px;
  letter-spacing: 2px;
  line-height: 40px;
}

.hero-links {
  position: relative;
  width: 100%;
  margin-top: 20px;
  
  display: flex;
  align-items: center;
}

.hero-links__link {
  position: relative;
  width: 60px;
  height: 60px;
  margin-right: 20px;
  
  border-radius: 8px;
  border: 1px solid #0071de60;
  cursor: pointer;
  transition: 1s cubic-bezier(0.075, 0.82, 0.165, 1) all;

  display: flex;
  justify-content: center;
  align-items: center;
}

.hero-links__link img {
  opacity: 0.8;
}

.hero-links__link:hover {
  border-color: #0071de;
  box-shadow: 0 0 8px 2px #0071de;
}

.hero-links__link:hover img {
  opacity: 1;
  filter: drop-shadow(0 0 8px #0071de);
}

@media (max-width: 800px) {
  .hero-text {
    position: relative;
    width: 100%;
    height: auto;
    margin: 0;
    padding: 20px;

    align-items: center;
  }

  .title {
    margin-bottom: 40px;
  }

  .hero-links {
    margin-top: 40px;
    justify-content: space-around;
  }
}

</style>
