<template>
  <div class="page faq">
    <div class="side-stripe left"></div>
    <div class="side-stripe right"></div>
    <div class="contactContainer">
       <h1>Reach us at: <a href="mailto:ratstackstudio@gmail.com">ratstackstudio@gmail.com</a></h1>
    </div>
  </div>
</template>

<script>
import screenSizeMixin from '@/mixins/screenSizeMixin';

export default {
  mixins: [screenSizeMixin],
  data() {
    return {
      
    };
  },
};
</script>

<style scoped>
.side-stripe {
    position: absolute; /* Position absolutely within the parent */
    top: 0;            /* Align to top */
    bottom: 0;         /* Stretch to bottom */
    width: 5%;       /* Width of the stripe */
    background: repeating-linear-gradient(
      135deg,
      rgb(155, 155, 155) 5px,
      rgb(155, 155, 155) 5px,
      transparent 10px,
      transparent 50px
    );
  }
  
  .left {
    left: 0;           /* Position on the left side */
  }
  
  .right {
    right: 0;          /* Position on the right side */
  }

  .page {
    min-height: 70vh;
    align-items: center;
    background-color: #ffffff;
    position: relative;
  }
.faq {
  display: flex;
  flex-direction: column;
}

.contactContainer {
  width: 70%;
  padding-top: 5rem;
  padding-bottom: 5rem;
  min-height: 60vh;
  text-align: center;
  justify-content: center;
  display: flex;
  align-items: center;
}

.accordion{
  border: #790606 solid 5px;
}
</style>
