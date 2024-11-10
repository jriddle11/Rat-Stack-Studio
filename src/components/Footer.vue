<template>
  <div class="footerContainer">
    <footer :class="isMobile ? 'footerSmall' : 'footer'">
      <div class="footer-section company-info">
        <h3>Studio</h3>
        <p>Careers</p>
        <p>Privacy Policy</p>
        <p>Terms of Service</p>
      </div>

      <div class="footer-section quick-links">
        <h3>Quick Links</h3>
        <p>Home</p>
        <p>FAQ</p>
        <p>About</p>
      </div>

      <div class="footer-section contact-info">
        <h3>Contact Us</h3>
        <p>Email: ratstackstudio@gmail.com</p>
      </div>

      <div class="footer-section social-media">
        <h3>Follow Us</h3>
        <i class="pi pi-facebook"></i>
        <i class="pi pi-twitter"></i>
        <i class="pi pi-instagram"></i>
        <i class="pi pi-linkedin"></i>
      </div>
    </footer>
  </div>
</template>

<script>
import screenSizeMixin from '@/mixins/screenSizeMixin';

export default {
  mixins: [screenSizeMixin],
};
</script>

<style scoped>
.footer {
  width: 100%;
  background-color: black;
  color: white;
  display: flex;
  justify-content: space-around;
  align-items: flex-start;
  padding: 20px;
  box-sizing: border-box;
}

.footerSmall{
  width: 100%;
  background-color: black;
  color: white;
  display: flex;
  justify-content: space-around;
  align-items: flex-start;
  padding: 20px;
  box-sizing: border-box;
  font-size: 0.6rem;
}

.footer-section {
  display: flex;
  flex-direction: column;
  gap: 5px;
}

.footer-section h3 {
  margin-bottom: 10px;
  font-weight: bold;
}

.social-media .pi {
  font-size: 1.5em;
  margin-right: 10px;
  cursor: pointer;
}

.footerContainer {
  border-top: solid #151515 2px;
}
</style>
