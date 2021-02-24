<template>
  <div class="home">

    <HeroText />

    <div class="projects-container">
      <a class="projects-header">Experience</a>
      <div class="project-container">
        <img class="project-container__link-icon" src="@/assets/google.svg" />
        <a class="project-container__title">Google (Software Engineer)</a>
        <a class="project-container__sub-title">Oct 2019 - Dec 2020</a>
        <a class="project-container__desc">
          Working on the Google Smart Displays and the Google Home App, I
          helped my team create experiences using Dart, Flutter, 
          and some proprietary Google web frameworks. My main work was on the 
          Google Home App experience for Automated Home Routines. 
          Fun fact: I signed my contract on the night of my 18th birthday 
          making me the youngest full-time engineer. And since I was told I 
          couldn't legally sign before 18, this record might be held for a while.
        </a>
      </div>
      <div class="project-container">
        <img class="project-container__link-icon" src="@/assets/storr.svg" />
        <a class="project-container__title">Storr (Software Engineer)</a>
        <a class="project-container__sub-title">Jul 2019 - Oct 2019</a>
        <a class="project-container__desc">
          As one of the first engineers in this SF-born startup, I focused on
          developing new features such as a cart, new UI, and updating the buying 
          experience for a React Native app focused on social buying and selling
          of recommended products. The idea of a P2P marketplace for products
          you can trust because your contacts signed off appealed to me. Also,
          this was one of the few startups willing to hire someone under 18 :D
        </a>
      </div>
      <div class="project-container">
        <img class="project-container__link-icon" src="@/assets/startup.svg" />
        <a class="project-container__title">Failed AI Startup (Co-Founder, CTO)</a>
        <a class="project-container__sub-title">Apr 2018 - Jul 2019</a>
        <a class="project-container__desc">
          At 16 I dropped out of high-school and moved to CA to start my own
          company. Both attempts (Cohereum, Levana) were focused on coding an 
          Auto-AI platform to make building custom machine learning 
          solutions easier for non-tech businesses. We raised a few million 
          and developed an end-to-end platform for building neural nets, but
          ultimately failed - largely due to my own shortcomings as a CTO. 
          Nonetheless, the experience taught me a great deal about perseverance, 
          company structure, law, technology, and machine learning.
        </a>
      </div>

      <a class="projects-header">Recent Projects</a>
      <div class="project-container clickable" @click="pytinder">
        <img class="project-container__link-icon" src="@/assets/github.svg" />
        <div class="project-container__title">
          PyTinder
        </div>
        <a class="project-container__desc">
          PyTinder is a fun side-project that aims to automate the entire 
          Tinder lifecycle, from swiping right to the date being setup.
          PyTinder uses Selenium to automate interaction with the Tinder web 
          interface and Seq2Seq LSTMs to chat with matched users.
        </a>
      </div>
      <div class="project-container clickable" @click="theia">
        <img class="project-container__link-icon" src="@/assets/github.svg" />
        <a class="project-container__title">Theia (ML Music Recommender)</a>
        <a class="project-container__desc">
          Built for a friend to advertise their songs on similar music, Theia 
          crawls YouTube Music sorting songs by "similarity" to a baseline. 
          Theia decides "similarity" by using the cosine distance between the
          second-to-last layer of a genre classifier CNN.
        </a>
      </div>
      <div class="project-container clickable" @click="elginbeloycom">
        <img class="project-container__link-icon" src="@/assets/github.svg" />
        <a class="project-container__title">elginbeloy.com</a>
        <a class="project-container__desc">
          My personal website - the one you're currently viewing. I built this
          version in VueJS, host it on Netlify, and have it open-source on Github.
          The older version was built in React, and before that plain old
          HTML/CSS/JQuery (remember the days before Node?).
        </a>
      </div>
      <div class="project-container clickable" @click="magic">
        <img class="project-container__link-icon" src="@/assets/github.svg" />
        <a class="project-container__title">Magic (A VueJS Game)</a>
        <a class="project-container__desc">
          A little - but fun - game I made entirely in VueJS. Fight monsters, 
          buy new spells, find items, travel, whole lots of stuff in this little
          SPA game! I originally made it for task management but it became a game.
        </a>
      </div>

      <a class="projects-header">Blog Posts</a>
      <div class="project-container">
        <img class="project-container__link-icon" src="@/assets/link.svg" />
        <a class="project-container__title">Start Trading Theories</a>
        <div class="project-container__links"></div>
        <a class="project-container__desc">
          "Stop Trading Back Tests, Start Trading Theories". A medium post
          on the difference between trading black-box models and trading 
          theories built on model back tests as validation.
        </a>
      </div>
    </div>
  </div>
</template>

<script>

import HeroText from "@/components/HeroText.vue";

export default {
  name: 'Home',
  components: {
    HeroText
  },
  methods: {
    pytinder: function () {   
      window.open("https://github.com/elginbeloy/PyTinder", "_blank");    
    },
    theia: function () {   
      window.open("https://github.com/elginbeloy/Theia", "_blank");    
    },
    elginbeloycom: function () {   
      window.open("https://github.com/elginbeloy/elginbeloycom", "_blank");    
    },
    magic: function () {   
      window.open("https://github.com/elginbeloy/Magic", "_blank");    
    },
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

.projects-container {
  position: absolute;
  top: 0%;
  right: 0%;
  width: 50%;
  height: auto;
  padding: 100px;

  overflow: none;

  display: flex;
  flex-direction: column;
}

.projects-header {
  color: #0071de;
  font-size: 32px;
  text-transform: uppercase;
  letter-spacing: 6px;
  margin-bottom: 20px;
  margin-top: 40px;
}

.clickable {
  cursor: pointer;
}

.project-container {
  position: relative;
  width: 100%;
  padding: 10px;
  margin-bottom: 20px;
  border-radius: 4px;
  border: 1px solid #0071de80;
  transition: 1s cubic-bezier(0.075, 0.82, 0.165, 1) all;
  opacity: 0.6;

  display: flex;
  flex-direction: column;

  &__link-icon {
    position: absolute;
    right: 10px;
    top: 10px;
    height: 20px;
  }

  &__title {
    font-size: 18px;
    color: #2ce692;
    margin-bottom: 10px;
  }

  &__sub-title {
    font-size: 12px;
    color: #ffffff;
    margin-bottom: 10px;
  }

  &__desc {
    font-size: 14px;
    line-height: 32px;
    color: #0071de;
    margin-bottom: 10px;
  }

  &:hover {
    transform: scale(1.05);
    border: 1px solid #0071de;
    opacity: 1;
  }
}

@media (max-width: 800px) {
  .home {
    padding: 20px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
  }

  .projects-container {
    position: relative;
    width: 600px;
  }
}
</style>