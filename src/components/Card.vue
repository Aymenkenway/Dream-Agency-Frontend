<template>
  <div>
    <swiper
      :slides-per-view="getSlidesPerView()"
      :space-between="50"
      :loop="true"
      :pagination="true"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      :autoplay="{ delay: 200, disableOnInteraction: false }"
    >
      <swiper-slide v-for="(slide, index) in slides" :key="index">
        <div class="box">
          <div class="rectangle">
            <div class="small-box">
              <div
                class="small-rectangle"
                :style="{ backgroundImage: `url(${slide.image})` }"
              ></div>
            </div>
            <h1 class="title">{{ slide.title }}</h1>
            <p class="lorem">
              {{ slide.text }}
            </p>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import SwiperCore, { Navigation, Pagination } from 'swiper'
import { Swiper, SwiperSlide } from 'swiper-vue2'

import 'swiper/swiper-bundle.css'

SwiperCore.use([Navigation, Pagination])

export default {
  name: 'CardComponent',
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      slides: [
        {
          title: 'WEBSITE DESIGN',
          text: 'Lorem Ipsum has been the industres standard dummy text ever since the 1500s',
          image: require('../assets/icons/website.png'),
        },
        {
          title: 'WEB DEVELOPMENT',
          text: 'Lorem Ipsum has been the industres standard dummy text ever since the 1500s',
          image: require('../assets/icons/computer.png'),
        },
        {
          title: 'MOBILE APP DEVELOPMENT',
          text: 'Lorem Ipsum has been the industres standard dummy text ever since the 1500s',
          image: require('../assets/icons/mobile.png'),
        },
        {
          title: 'MARKETING',
          text: 'Lorem Ipsum has been the industres standard dummy text ever since the 1500s',
          image: require('../assets/icons/rocket.png'),
        },
        {
          title: 'WEBSITE DESIGN',
          text: 'Lorem Ipsum has been the industres standard dummy text ever since the 1500s',
          image: require('../assets/icons/website.png'),
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
    getSlidesPerView() {
      // Adjust slides per view based on screen size
      if (window.innerWidth < 576) {
        return 1
      } else if (window.innerWidth < 1110) {
        return 2
      } else if (window.innerWidth < 1495) {
        return 3
      }
      {
        return 4
      }
    },
  },
}
</script>

<style scoped>
.box .rectangle {
  width: 308px;
  height: 192px;
  border-radius: 10px;
  box-shadow: 0px 0px 9px 2px rgba(0, 0, 0, 0.05);
  padding: 10px 0px 0px 10px;
}
.small-box {
  width: 52px;
  height: 48px;
}

.small-box .small-rectangle {
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  width: 52px;
  height: 48px;
  top: 0;
  left: 0;
  background-color: #ffded4;
  border-radius: 10px;
  background-image: url(../assets/icons/website.png);
  background-position: center;
  background-repeat: no-repeat;
}
.lorem {
  color: rgba(51, 27, 59, 0.66);
  font-size: 15px;
  font-family: 'Hind Vadodara-Light', sans-serif;
  font-weight: 300;
  line-height: 21.79px;
  letter-spacing: 0.3px;
  word-wrap: break-word;
}
.title {
  margin: 10px 0 10px 0;
  color: #331b3b;
  font-size: 16px;
  font-weight: 700;
  letter-spacing: 0.88px;
  left: 0;
  top: 0;
  line-height: 21.8px;
  font-family: 'Hind Vadodara', sans-serif;
  white-space: nowrap;
}
@media (max-width: 767px) {
  .box .rectangle {
    width: 100%; /* Full width on smaller screens */
  }
  .title {
    font-size: 12px;
  }
}

@media (max-width: 575px) {
}
</style>
