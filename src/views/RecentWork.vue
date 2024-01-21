<template>
  <div class="swiper-contain">
    <div class="sub-container pb-8 pt-5 flex flex-row justify-between">
      <div class="titles flex-1 ml-10">
        <span class="OurRecentWork">Our Recent Work<br /></span
        ><span class="ByOurExperts">By Our Experts</span>
      </div>
      <div class="flex-1 flex flex-row justify-end">
        <p class="paragraph w-4/5">
          Lorem Ipsum has been the industry's standard dummy text ever since the
          1500s, when an unknown printer took a galley of type and scrambled it
          to make a type specimen book.
        </p>
      </div>
    </div>
    <div class="flex flex-row justify-end">
      <SecondCard class="cards h-full w-4/5" />
    </div>
  </div>
</template>

<script>
import SecondCard from '@/components/SecondCard.vue'
export default {
  name: 'RecentWork',
  components: { SecondCard },
}
</script>

<style scoped>
.swiper-contain {
  background-image: url('../assets/icons/swiper-background2.png');
  background-repeat: no-repeat;
  background-position: right;
  border-top-left-radius: 158px;
  height: 500px;
}
.OurRecentWork {
  color: #331b3b;
  font-size: 48px;
  font-family: 'Hind Vadodara', sans-serif;
  font-weight: 700;
  line-height: 51.02px;
  word-wrap: break-word;
}

.ByOurExperts {
  color: #331b3b;
  font-size: 48px;
  font-family: 'Hind Vadodara', sans-serif;
  font-weight: 300;
  line-height: 51.02px;
  word-wrap: break-word;
}
.paragraph {
  color: #331b3b;
  font-size: 17px;
  font-family: 'Hind Vadodara', sans-serif;
  font-weight: 400;
  line-height: 24.87px;
  letter-spacing: 0.34px;
  word-wrap: break-word;
}
@media (max-width: 768px) {
  .swiper-contain {
    background-position: left;
    height: 600px;
  }

  .OurRecentWork {
    font-size: 40px;
  }
  .ByOurExperts {
    font-size: 40px;
  }
}
@media (max-width: 590px) {
  .swiper-contain {
    margin: 80px 0px 0px 0px;
  }
  .sub-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-bottom: 25px;
    padding: 0;
  }
  .flex-1 {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .paragraph {
    margin: 20px 0px 20px 0px;
  }
  .cards {
    width: 100%;
    margin-bottom: 100px;
  }
  .titles {
    margin: 0;
  }
}
</style>
