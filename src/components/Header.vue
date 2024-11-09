<script>
import 'primeicons/primeicons.css';

import Toolbar from 'primevue/toolbar';
import Menu from 'primevue/menu';
import Button from 'primevue/button';

import screenSizeMixin from '@/mixins/screenSizeMixin';

export default {
  mixins: [screenSizeMixin],
  components: {
    Toolbar,
    Menu,
    Button,
  },
  methods: {
        navigateTo(path) {
        this.$router.push(path);
      },
  },
  data() {
    return {
      navMenu: [
        { label: 'Home', to: '/', command: () => this.navigateTo('/') },
        { label: 'FAQ', to: '/faq', command: () => this.navigateTo('/faq') },
        { label: 'Contact', to: '/contact', command: () => this.navigateTo('/contact') },
      ],
      cartMenu: [
        { label: 'View Cart', to: '/cart', command: () => this.navigateTo('/cart') },
        { label: 'Clear', to: '/cart' },
      ],
    };
  },
};
</script>

<template>
  <div class="headerContainer">
    <header>
      <Toolbar
        style="padding: 1rem 1rem 1rem 1rem; background-color: black; border: none; border-radius: 0; border-bottom: solid #151515 2px;"
      >
        <template #start>
          <RouterLink to="/" class="titleLink">
            <div class="titleImageSmall" v-if="isMobile"></div>
            <div class="titleImage" v-if="!isMobile"/>
          </RouterLink>
          
          <div v-if="!isMobile" class="flex items-center gap-2">
            <Button label="Home" as="router-link" to="/" severity="contrast" style="background-color: transparent;" class="navItem" />
            <Button label="FAQ" as="router-link" to="/faq" severity="contrast" style="background-color: transparent;" class="navItem" />
            <Button label="Contact" as="router-link" to="/contact" severity="contrast" style="background-color: transparent;" class="navItem" />
          </div>
        </template>

        <template #end>
          <!--<Menu :model="cartMenu" popup ref="cart" />
          <Button icon="pi pi-shopping-cart" @click="$refs.cart.toggle($event)" class="menu" severity="contrast" size="large"/>-->
          <Menu v-if="isMobile" :model="navMenu" popup ref="menu" />
          <Button v-if="isMobile" icon="pi pi-bars" @click="$refs.menu.toggle($event)" class="menu" severity="contrast" size="large"/>
        </template>
      </Toolbar>
    </header>
  </div>
</template>

<style scoped>
.titleImage {
  height: 5.2rem;
  width: 22.5rem;
  background-image: url('./images/Title.png');
  background-size: cover;
  transition: background-image 0.3s ease;
}
.titleImage:hover {
  background-image: url('./images/TitleGlow.png');
  cursor: pointer;
}
.titleImageSmall {
  height: 2.106rem;
  width: 9.1125rem;
  background-image: url('./images/Title.png');
  background-size: cover;
  transition: background-image 0.3s ease;
}
.titleImageSmall:hover {
  background-image: url('./images/TitleGlow.png');
  cursor: pointer;
}
.navItem {
  text-decoration: none;
}
.titleLink {
  margin-left: 3vw;
  margin-right: 3vw;
}
.headerContainer {
  z-index: 1000;
}
.menu {
  color:white;
  font-size: 1.2rem;
  margin-right: 2vw;
  background-color: transparent;
}
</style>
