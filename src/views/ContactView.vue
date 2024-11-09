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
import '@/styles/page.css'

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
