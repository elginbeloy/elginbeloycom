<template>
  <div class="projects-container">
    <img class="cloud cloud--flipped" src="@/assets/cloud.png" style="top: 43%; left: -8%; width: 43%; opacity: 0.01;" />
    <img class="cloud" src="@/assets/cloud.png" style="top: 51%; left: 89%; width: 13%; opacity: 0.02;" />
    <img class="cloud cloud--flipped" src="@/assets/cloud.png" style="top: 15%; left: -5%; width: 23%; opacity: 0.03;" />
    <img class="cloud" src="@/assets/cloud.png" style="top: 13%; left: 28%; width: 6%; opacity: 0.03;" />
    <img class="cloud cloud--flipped" src="@/assets/cloud.png" style="top: 8%; left: 90%; width: 22%; opacity: 0.04;" />
    <img class="cloud" src="@/assets/cloud.png" style="top: 88%; left: 36%; width: 16%; opacity: 0.04;" />
    <img class="cloud cloud--flipped" src="@/assets/cloud.png" style="top: 108%; left: 73%; width: 4%; opacity: 0.05;" />
    <img class="cloud" src="@/assets/cloud.png" style="top: 31%; left: 82%; width: 14%; opacity: 0.05;" />
    <img class="cloud cloud--flipped" src="@/assets/cloud.png" style="top: 63%; left: 31%; width: 8%; opacity: 0.06;" />
    <img class="cloud cloud--flipped" src="@/assets/cloud.png" style="top: 27%; left: 43%; width: 12%; opacity: 0.06;" />
    
    <a class="projects-header">Experience</a>
    <div class="project-container">
      <a class="project-container__title">Google (Software Engineer)</a>
      <a class="project-container__sub-title">Oct 2019 - Dec 2020</a>
      <a class="project-container__sub-title">Jul 2020 - Present</a>
      <a class="project-container__desc">
        After first joining I worked on built-in software for the newest 
        generation of Google Smart Displays and some pages for Routines in
        the Google Home App. I helped my team create experiences using Dart, 
        Flutter, JavaScript, and some proprietary Google frameworks. 
        
        Now I primarily work on Google Payments pages which are used in 
        Google Play, Youtube, and other integrating apps / websites.
      </a>
    </div>
    <div class="project-container">
      <a class="project-container__title">Quant Day Trader</a>
      <a class="project-container__sub-title">Dec 2020 - Present</a>
      <a class="project-container__desc">
        I study different approaches to trading / asset management, 
        focusing heavily on machine learning + alternative data use cases. 
        Currently I'm studying ML-based risk management, portfolio construction,
        strategy backtesting, and statistical significance testing. 
        I use my own home-coded, Python based backtesting system which 
        utilizes tick level data from polygon.io. I mainly read online articles,
        papers, and books from Chen and Lopez de Prado (with some technical analysis
        though I quickly lost interest with poor backtest results).
      </a>
    </div>
    <div class="project-container">
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
    <div class="project-container clickable" @click="theia">
      <img class="project-container__link-icon" src="@/assets/arrow.svg" />
      <div class="project-container__lang-icons">
        <img class="project-container__lang-icon" src="@/assets/python.png" />
        <img class="project-container__lang-icon" src="@/assets/selenium.png" />
        <img class="project-container__lang-icon" src="@/assets/keras.png" />
      </div> 
      <a class="project-container__title">Theia</a>
      <a class="project-container__sub-title">Python, Selenium, Keras</a>
      <a class="project-container__desc">
        A ML approach to measuring music similarity I built for a friend 
        to increase click-through rates and decrease advertising cost for 
        their music. Theia crawls YouTube Music downloading songs to 
        compare to a baseline spitting out the top-N closest songs. 
        Theia decides "similarity" by using the cosine distance between the
        second-to-last layer of a genre classification Convolutional Neural Net
        that takes in the music spectrograms as visual input data.
      </a>
    </div>
    <div class="project-container clickable" @click="pytinder">
      <img class="project-container__link-icon" src="@/assets/arrow.svg" />
      <div class="project-container__lang-icons">
        <img class="project-container__lang-icon" src="@/assets/python.png" />
        <img class="project-container__lang-icon" src="@/assets/selenium.png" />
      </div>
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
    <div class="project-container clickable" @click="elginbeloycom">
      <img class="project-container__link-icon" src="@/assets/arrow.svg" />
      <div class="project-container__lang-icons">
        <img class="project-container__lang-icon" src="@/assets/javascript.png" />
        <img class="project-container__lang-icon" src="@/assets/vue.png" />
      </div>
      <a class="project-container__title">elginbeloy.com</a>
      <a class="project-container__sub-title">JavaScript, Vue</a>
      <a class="project-container__desc">
        My personal website - the one you're currently viewing. I built this
        version in VueJS, host it on Netlify, and have it open-source on Github.
        The older version was built in React, and before that plain old
        HTML/CSS/JQuery (remember the days before Node?).
      </a>
    </div>
    <div class="project-container clickable" @click="magic">
      <img class="project-container__link-icon" src="@/assets/arrow.svg" />
      <div class="project-container__lang-icons">
        <img class="project-container__lang-icon" src="@/assets/javascript.png" />
        <img class="project-container__lang-icon" src="@/assets/vue.png" />
      </div>
      <a class="project-container__title">Magic (A VueJS Game)</a>
      <a class="project-container__sub-title">JavaScript, Vue</a>
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

<style scoped>

@keyframes cloud_floating {
  0% { 
    transform: none;
  }
  50% {
    transform: translateX(-150px) translateY(-150px);
  }
  100% { 
    transform: none;
  }
}

@keyframes cloud_floating_flipped {
  0% { 
    transform: scaleX(-1);
  }
  50% {
    transform: translateX(-150px) translateY(-150px) scaleX(-1);
  }
  100% { 
    transform: scaleX(-1);
  }
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

.cloud {
  position: fixed;
  filter: drop-shadow(0 0.5rem 0.5rem #0071de);
  z-index: 0;
  touch-action: none;
  -ms-touch-action: none;
  -moz-user-select: none;
  -webkit-user-select: none;
  user-select: none;

  animation: cloud_floating 30s linear infinite;
  -ms-animation: cloud_floating 30s linear infinite;
  -moz-animation: cloud_floating 30s linear infinite;
  -webkit-animation: cloud_floating 30s linear infinite;
}

.cloud--flipped {
  animation: cloud_floating_flipped 30s linear infinite;
  -ms-animation: cloud_floating_flipped 30s linear infinite;
  -moz-animation: cloud_floating_flipped 30s linear infinite;
  -webkit-animation: cloud_floating_flipped 30s linear infinite;
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
}

.project-container__link-icon {
  position: absolute;
  right: 15px;
  bottom: 10px;
  height: 25px;
  transition: 0.2s linear all;
}

.project-container:hover .project-container__link-icon {
  right: 10px;
  transform: scale(1.02);
}

.project-container__lang-icons {
  position: absolute;
  top: 15px;
  right: 0px;
  
  display: flex;
  align-items: center;
}

.project-container__lang-icon {
  position: relative;
  margin-right: 15px;

  height: 30px;
  opacity: 0.6;
  transition: 0.2s linear all;
}

.project-container:hover .project-container__lang-icon {
  opacity: 1;
}

.project-container__title {
  font-size: 20px;
  color: #2ce692;
  margin-bottom: 10px;
}

.project-container__sub-title {
  font-size: 14px;
  color: #ffffff;
  margin-bottom: 10px;
}

.project-container__desc {
  font-size: 16px;
  line-height: 32px;
  color: #0071de;
  margin-bottom: 10px;
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