<template>
  <div class="page faq">
    <div class="side-stripe left"></div>
    <div class="side-stripe right"></div>
    <div class="questionsContainer">
      <Accordion multiple class="accordion">
        <AccordionPanel v-for="(item, index) in faqItems" :key="index" :value="index">
          <AccordionHeader>{{ item.question }}</AccordionHeader>
          <AccordionContent>
            <p class="m-0">{{ item.answer }}</p>
          </AccordionContent>
        </AccordionPanel>
      </Accordion>
    </div>
  </div>
</template>

<script>

import Accordion from 'primevue/accordion';
import AccordionPanel from 'primevue/accordionpanel';
import AccordionHeader from 'primevue/accordionheader';
import AccordionContent from 'primevue/accordioncontent';

import screenSizeMixin from '@/mixins/screenSizeMixin';

export default {
  mixins: [screenSizeMixin],
  data() {
    return {
      faqItems: [
        { question: "What do you do?", answer: "Rat Stack Studio was created to produce video games and video game assets." },
        { question: "Do you do commisions?", answer: "Yes! If you would like to commision a game asset please email us at ratstackstudio@gmail.com with details of your request." },
        { question: "Where can I go for help?", answer: "Please send all questions and concerns to ratstackstudio@gmail.com and we will do our best to help." },
      ]
    };
  },
  components: {
    Accordion,
    AccordionPanel,
    AccordionHeader,
    AccordionContent,
  }
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

.questionsContainer {
  width: 70%;
  padding-top: 5rem;
  padding-bottom: 5rem;
  min-height: 60vh;
}

.accordion{
  border: #0b9ac5 solid 5px;
}
</style>
