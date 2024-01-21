<template>
  <div class="app">
    <HeaderComponent class="mt-8 mb-8" />
    <HeroView />
    <FirstSwiper class="mt-20" />
    <AboutUs class="mt-12" />
    <RecentWork class="mt-20" />
    <Testimonials class="mt-20" />
    <Footer class="mt-20" />
  </div>
</template>

<script>
import HeaderComponent from './components/Header.vue'
import HeroView from './views/Hero.vue'
import AboutUs from './views/AboutUs.vue'
import FirstSwiper from './views/FirstSwiper.vue'
import RecentWork from './views/RecentWork.vue'
import Testimonials from './views/Testimonials.vue'
import Footer from './views/Footer.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    HeroView,
    FirstSwiper,
    AboutUs,
    RecentWork,
    Testimonials,
    Footer,
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Hind+Vadodara:wght@300;400;500;700&display=swap');

.app {
  font-family: Avenir, Helvetica, Arial, Hind-Vadodara, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background-image: url('./assets/icons/Vector1.png');
  background-repeat: no-repeat;
  background-position: right top;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

@media (max-width: 1600px) {
  .app {
    overflow: hidden;
  }
}
</style>
