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
  import '../styles/page.css';
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
  