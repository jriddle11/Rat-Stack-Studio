<template>
    <div class="page error">
      <div class="side-stripe left"></div>
      <div class="side-stripe right"></div>
      <div class="content">
        <h1 style="margin-bottom: 3rem; color:#0b9ac5">THIS PAGE DOES NOT EXIST</h1>
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
  .error{
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .content{
    margin-top: 10rem;
    width: 80%;
    
    align-items: center;
    text-align: center;
    justify-content: center
  }
  </style>
  