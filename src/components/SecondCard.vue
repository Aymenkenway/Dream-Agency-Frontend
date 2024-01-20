<template>
  <div>
    <swiper
      :slides-per-view="3"
      :space-between="50"
      :loop="true"
      :pagination="true"
      :navigation="true"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
    >
      <swiper-slide v-for="(slide, index) in slides" :key="index">
        <div class="box">
          <div class="rectangle">
            <div
              class="image"
              :style="{ backgroundImage: `url(${slide.image})` }"
            ></div>
            <h1 class="title">{{ slide.title }}</h1>
          </div>
          <div class="sub-rectangle">
            <div
              class="image"
              :style="{ backgroundImage: `url(${slide.image})` }"
            ></div>
            <div class="view">View Work</div>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import SwiperCore, { Navigation, Pagination } from 'swiper'
import { Swiper, SwiperSlide } from 'swiper-vue2'

// Import Swiper styles
import 'swiper/swiper-bundle.css'

SwiperCore.use([Navigation, Pagination])

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      slides: [
        {
          title: 'UI Soup',
          image: require('../assets/icons/screenshot1.png'),
        },
        {
          title: 'Goldcrown Labs',
          image: require('../assets/icons/screenshot2.png'),
        },
        {
          title: 'Close Concierge',
          image: require('../assets/icons/screenshot3.png'),
        },
        {
          title: 'UI Soup',
          image: require('../assets/icons/screenshot2.png'),
        },
        {
          title: 'Goldcrown Labs',
          image: require('../assets/icons/screenshot2.png'),
        },
      ],
    }
  },

  methods: {
    onSwiper(swiper) {
      console.log(swiper)
    },
    onSlideChange() {
      console.log('slide change')
    },
  },
}
</script>

<style lang="scss" scoped>
.box {
  padding: 10px 10px 0px 10px;
  display: flex;
  flex-direction: row;
  background-color: #fff;
  border-radius: 3%;
  justify-content: center;
}

.box .rectangle {
  display: flex;
  justify-content: center;
  flex-direction: column;
  width: 250px;
  height: 298px;
}

.box .sub-rectangle {
  display: flex;
  justify-content: center;
  flex-direction: column;
  width: 100px;
  height: 298px;
  border-radius: 10px;
}
.title {
  margin: 20px 0 20px 0;
  color: #331b3b;
  font-size: 24px;
  font-weight: 700;
  letter-spacing: 0.88px;
  line-height: 21.8px;
  font-family: 'Hind Vadodara', sans-serif;
}

.image {
  flex: 1;
  height: 100%;
  background-size: cover;
  background-position: center;
}

.view {
  margin: 20px 0 20px 0;
  width: 65%;
  height: 6%;
  border-radius: 100px;
  border: 2px #343434 solid;
  margin-left: 15px;
  text-align: center;
  font-size: 10px;
}
</style>
