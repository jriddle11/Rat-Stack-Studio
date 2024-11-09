<script>
import '../styles/page.css'
import screenSizeMixin from '@/mixins/screenSizeMixin';

export default {
  mixins: [screenSizeMixin],
  data() {
    return {
    };
  },
  methods: {
    scrollToAbout() {
      const aboutSection = document.getElementById("about");
      if (aboutSection) {
        aboutSection.scrollIntoView({ behavior: "smooth" });
      }
    }
  },
}
</script>

<template>
    <div :class="!isMobile ? 'homeContainer' : 'homeContainerSmall'">
      <div class="background" v-if="!isMobile"/>
      <div class="backgroundSmall" v-if="isMobile"/>
      <div class="pageButton" @click="scrollToAbout">
          <h1>About ⇓</h1>
      </div>
    </div>
    <div id="about" class="aboutContainer">
      <div :class="isMobile ? 'aboutContentSmall' : 'aboutContent'">
          <h1 v-if="!isMobile">Rat Stack Studio</h1>
          <h3 v-else>Rat Stack Studio</h3>
          <p style="margin: 10px;">We are a passionate indie studio focused on creating games and high-quality game assets. We blend creativity and technical expertise to craft great experiences that resonate with players. 
            Join us on our path to creating unforgettable worlds, one game and asset at a time.</p>
      </div>
    </div>
</template>

<style scoped>
  .homeContainer{
    width: 100%;
    height: 85vh;
    background-color: black;
    justify-content: center;
    align-items: center;
    display: flex;
    position: relative;
  }
  .homeContainerSmall{
    width: 100%;
    height: 65vh;
    background-color: black;
    justify-content: center;
    align-items: center;
    display: flex;
    position: relative;
  }
  .background{
    height: 512px;
    width: 512px;
    background-image: url('../components/images/Kitchen1024.png');
    transition: background-image 0.3s ease;
    background-size: contain
    
  }
  .backgroundSmall{
    height: 256px;
    width: 256px;
    background-image: url('../components/images/Kitchen1024.png');
    transition: background-image 0.3s ease;
    background-size: contain
    
  }
  .pageButton{
    position: absolute;
    width: 250px;
    height: 55px;
    bottom: 0;
    background-color: #0b9ac5;
    color:white;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .pageButton:hover{
    background-color: #0dc6ff;
    cursor: pointer;
  }

  .aboutContainer{
    width: 100%;
    min-height: 40vh;
    background-color: #ffffff;
    justify-content: center;
    align-items: center;
    display: flex;
  }
  .aboutContent{
    width: 60%;
    min-height: 20vh;
    background-color: white;
    border: #0b9ac5 solid 5px;
    text-align: center;
    color: black;
  }
  .aboutContentSmall{
    width: 90%;
    height: 20vh;
    background-color: white;
    border: #0b9ac5 solid 5px;
    text-align: center;
    color: black;
  }

</style>
