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
      I'm currently working on ML algorithms for my own day trading practice, 
      but am open to new opportunities! :)
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
  }
}

</script>

<style scoped lang="scss">

.hero-text {
  position: -webkit-sticky;
  position: sticky;
  top: 0%;
  left: 0%;
  height: 100%;
  width: 50%;
  padding: 100px;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.green-text {
  color: #2ce692;
}

.title {
  position: relative;
  width: 100%;

  color: #0071de;
  font-size: 76px;
  font-weight: 100;
  letter-spacing: 8px;
  margin-bottom: 20px;
}

.subtitle {
  position: relative;
  width: 100%;

  color: #0071de;
  font-size: 18px;
  letter-spacing: 2px;
  line-height: 36px;
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

  img {
    opacity: 0.5;
  }

  &:hover {
    border-color: #0071de;
    box-shadow: 0 0 8px 2px #0071de60;
    transform: scale(1.05);

    img {
      opacity: 1;
      filter: drop-shadow(0 0 8px #0071de);
    }
  }
}

@media (max-width: 800px) {
  .hero-text {
    position: relative;
    width: 100%;
    height: auto;
    margin: 0;
  }

  .title {
    font-size: 36px;
    margin-bottom: 40px;
  }

  .hero-links {
    margin-top: 40px;
    justify-content: space-around;
  }
}

</style>
