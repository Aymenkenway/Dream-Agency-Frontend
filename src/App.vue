<template>
  <div class="app">
    <HeaderComponent />
    <Main />
    <Review />
    <RecentWork />
    <HireMe />
    <EmailMe />
    <Brands />
    <FeedbacksView />
    <Footer />
  </div>
</template>

<script>
import HeaderComponent from './components/Header.vue'

import Main from './views/Main.vue'
import Review from './views/Review.vue'
import RecentWork from './views/RecentWork.vue'
import HireMe from './views/HireMe.vue'
import EmailMe from './views/EmailMe.vue'
import Brands from './views/Brands.vue'
import FeedbacksView from './views/Feedbacks.vue'
import Footer from './views/Footer.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    Main,
    Review,
    RecentWork,
    HireMe,
    EmailMe,
    Brands,
    FeedbacksView,
    Footer,
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,700;1,100;1,200;1,300;1,400;1,600;1,700&display=swap');

.app {
  font-family: 'Poppins', sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
