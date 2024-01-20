<template>
  <div class="swiper-contain flex flex-col justify-around">
    <div class="flex flex-col items-center">
      <span class="what-we-do">What We Do<br /></span
      ><span class="for-you-business">For Your Business</span>
    </div>
    <div class="flex flex-row justify-end">
      <Card class="h-full w-4/5" />
    </div>
  </div>
</template>

<script>
import Card from '../components/Card.vue'

export default {
  name: 'FirstSwiperView',
  components: {
    Card,
  },
}
</script>

<style scoped>
.swiper-contain {
  height: 500px;
  background-image: url(../assets/icons/swiper-background.png);
  background-repeat: no-repeat;
}
.what-we-do {
  color: #331b3b;
  font-size: 48px;
  font-family: Hind Vadodara;
  font-weight: 700;
  line-height: 51.02px;
  word-wrap: break-word;
}

.for-you-business {
  color: #331b3b;
  font-size: 48px;
  font-family: Hind Vadodara;
  font-weight: 300;
  line-height: 51.02px;
  word-wrap: break-word;
}
</style>
