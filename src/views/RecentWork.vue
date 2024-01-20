<template>
  <div class="swiper-contain ml-10">
    <div class="pb-12 pt-12 flex flex-row justify-between">
      <div class="flex-1">
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
      <SecondCard class="h-full w-4/5" />
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
  height: 500px;
}
.OurRecentWork {
  color: #331b3b;
  font-size: 48px;
  font-family: Hind Vadodara;
  font-weight: 700;
  line-height: 51.02px;
  word-wrap: break-word;
}

.ByOurExperts {
  color: #331b3b;
  font-size: 48px;
  font-family: Hind Vadodara;
  font-weight: 300;
  line-height: 51.02px;
  word-wrap: break-word;
}
.paragraph {
  color: #331b3b;
  font-size: 17px;
  font-family: Hind Vadodara;
  font-weight: 400;
  line-height: 24.87px;
  letter-spacing: 0.34px;
  word-wrap: break-word;
}
</style>
