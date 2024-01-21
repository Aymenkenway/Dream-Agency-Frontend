<template>
  <div class="swiper-contain flex flex-col justify-around">
    <div class="flex flex-col items-center">
      <span class="what-we-do">What We Do<br /></span
      ><span class="for-you-business">For Your Business</span>
    </div>
    <div class="card-container w-11/12 flex flex-row self-end">
      <Card class="card h-full md:w-full" />
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
  font-family: 'Hind Vadodara', sans-serif;
  font-weight: 700;
  line-height: 51.02px;
  word-wrap: break-word;
}

.for-you-business {
  color: #331b3b;
  font-size: 48px;
  font-family: 'Hind Vadodara', sans-serif;
  font-weight: 300;
  line-height: 51.02px;
  word-wrap: break-word;
}
/* here screen */
@media (max-width: 768px) {
  .swiper-contain {
    height: 400px;
  }
  .flex-row {
    flex-direction: row; /* Change flex direction to column on smaller screens */
  }

  .card {
    width: 70%;
  }
}

@media (max-width: 520px) {
  .card {
    width: 90%;
  }
  .swiper-contain {
    height: 400px;
    padding-top: 30px;
    border-top-right-radius: 158px;
  }
  .flex-row {
    flex-direction: row; /* Change flex direction to column on smaller screens */
  }

  .card-container {
    justify-content: center;
  }
  .what-we-do {
    font-size: 40px;
  }
  .for-you-business {
    font-size: 40px;
  }
}
</style>
