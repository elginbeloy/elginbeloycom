<template>
  <div class="projects-container">
    <img class="cloud" src="@/assets/cloud.png" style="top: 120px; left: 60px; width: 390px; opacity: 0.02;" />
    <img class="cloud" src="@/assets/cloud.png" style="top: 600px; left: 820px; width: 140px; opacity: 0.03;" />
    <img class="cloud" src="@/assets/cloud.png" style="top: 40px; right: 480px; width: 220px; opacity: 0.04;" />
    <img class="cloud" src="@/assets/cloud.png" style="bottom: 30px; left: 400px; width: 460px; opacity: 0.04;" />
    <img class="cloud" src="@/assets/cloud.png" style="top: 130px; right: 20px; width: 340px; opacity: 0.05;" />
    <img class="cloud" src="@/assets/cloud.png" style="top: 600px; right: 420px; width: 160px; opacity: 0.06;" />
    <img class="cloud" src="@/assets/cloud.png" style="top: 900px; right: 240px; width: 280px; opacity: 0.06;" />
    
    <a class="projects-header">Experience</a>
    <div class="project-container">
      <img class="project-container__bg-icon" src="@/assets/google.svg" />
      <a class="project-container__title">Google (Software Engineer)</a>
      <a class="project-container__sub-title">Oct 2019 - Dec 2020</a>
      <a class="project-container__desc">
        Working on the Google Smart Displays and the Google Home App, I
        helped my team create experiences using Dart, Flutter, 
        and some proprietary Google web frameworks. My main work was on the 
        Google Home App experience for Automated Home Routines.
      </a>
    </div>
    <div class="project-container">
      <img class="project-container__bg-icon" src="@/assets/storr.svg" />
      <a class="project-container__title">Storr (Software Engineer)</a>
      <a class="project-container__sub-title">Jul 2019 - Oct 2019</a>
      <a class="project-container__desc">
        As one of the early engineers in this SF-born startup, I focused on
        developing new features such as a cart, new UI, and updating the buying 
        experience for a React Native app focused on social buying and selling
        of recommended products.
      </a>
    </div>
    <div class="project-container">
      <img class="project-container__bg-icon" src="@/assets/startup.svg" />
      <a class="project-container__title">Defunct AI Startup (Co-Founder, CTO)</a>
      <a class="project-container__sub-title">Apr 2018 - Jul 2019</a>
      <a class="project-container__desc">
        At 16 I dropped out of high-school and moved to CA to start my own
        company. Both attempts (Cohereum & Levana) were focused on coding an 
        Auto-ML platform to make building custom machine learning 
        solutions easier for non-tech businesses. We raised a few million USD
        and developed an end-to-end platform for building neural nets, but
        ultimately failed. Nonetheless, the experience taught me a great deal 
        about perseverance, company structure, law, technology, and machine learning.
      </a>
    </div>

    <a class="projects-header">Recent Projects</a>
    <div class="project-container">
      <img class="project-container__bg-icon" src="@/assets/python.png" />
      <img class="project-container__link-icon clickable" src="@/assets/arrow.svg" @click="pytinder" />
      <div class="project-container__title">
        PyTinder
      </div>
      <a class="project-container__sub-title">Python, Selenium</a>
      <a class="project-container__desc">
        PyTinder is a fun side-project that aims to automate the entire 
        Tinder lifecycle, from swiping right to the date being setup.
        PyTinder uses Selenium to automate interaction with the Tinder web 
        interface and Seq2Seq LSTMs to chat with matched users.
      </a>
    </div>
    <div class="project-container">
      <img class="project-container__bg-icon" src="@/assets/python.png" />
      <img class="project-container__link-icon clickable" src="@/assets/arrow.svg" @click="theia" />
      <a class="project-container__title">Theia (ML Music Recommender)</a>
      <a class="project-container__sub-title">Python</a>
      <a class="project-container__desc">
        Built for a friend to advertise their songs on similar music, Theia 
        crawls YouTube Music sorting songs by "similarity" to a baseline. 
        Theia decides "similarity" by using the cosine distance between the
        second-to-last layer of a genre classifier CNN.
      </a>
    </div>
    <div class="project-container">
      <img class="project-container__bg-icon" src="@/assets/vue.png" />
      <img class="project-container__link-icon clickable" src="@/assets/arrow.svg" @click="elginbeloycom" />
      <a class="project-container__title">elginbeloy.com</a>
      <a class="project-container__sub-title">JavaScript, Vue, Less</a>
      <a class="project-container__desc">
        My personal website - the one you're currently viewing. I built this
        version in VueJS, host it on Netlify, and have it open-source on Github.
        The older version was built in React, and before that plain old
        HTML/CSS/JQuery (remember the days before Node?).
      </a>
    </div>
    <div class="project-container">
      <img class="project-container__bg-icon" src="@/assets/vue.png" />
      <img class="project-container__link-icon clickable" src="@/assets/arrow.svg" @click="magic" />
      <a class="project-container__title">Magic (A VueJS Game)</a>
      <a class="project-container__sub-title">JavaScript, Vue, Less</a>
      <a class="project-container__desc">
        A little - but fun - game I made entirely in VueJS. Fight monsters, 
        buy new spells, find items, travel, whole lots of stuff in this little
        SPA game! I originally made it for task management but it became a game.
      </a>
    </div>
  </div>
</template>

<script>

export default {
  name: 'ProjectsContainer',
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

.cloud {
  position: fixed;
  filter: drop-shadow(0 0.5rem 0.5rem #0071de);
  z-index: 0;
  touch-action: none;
  -ms-touch-action: none;
  -moz-user-select: none;
  -webkit-user-select: none;
  user-select: none;
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
  padding: 14px;
  margin-top: 20px;
  margin-bottom: 20px;
  background-color: #191919;
  border: 1px solid #0071de;
  border-radius: 4px;
  transform: scale(1.05);
  transition: 1s cubic-bezier(0.075, 0.82, 0.165, 1) all;
  overflow: hidden;
  overflow-x: hidden;
  overflow-y: hidden;

  display: flex;
  flex-direction: column;

  &__bg-icon {
    position: absolute;
    right: -30px;
    top: -20px;
    height: calc(100% + 40px);
    opacity: 0.04;
    z-index: 0;
    touch-action: none;
    -ms-touch-action: none;
    -moz-user-select: none;
    -webkit-user-select: none;
    user-select: none;
  }

  &__link-icon {
    position: absolute;
    right: 13px;
    bottom: 10px;
    height: 25px;
    transition: 0.2s linear all;

    &:hover {
      right: 10px;
    }
  }

  &__title {
    font-size: 20px;
    color: #2ce692;
    margin-bottom: 10px;
  }

  &__sub-title {
    font-size: 14px;
    color: #ffffff;
    margin-bottom: 10px;
  }

  &__desc {
    font-size: 16px;
    line-height: 32px;
    color: #0071de;
    margin-bottom: 10px;
  }
}

@media (max-width: 800px) {
  .projects-container {
    position: relative;
    width: 100%;
    height: auto;
    padding: 20px;
  }
}
</style>