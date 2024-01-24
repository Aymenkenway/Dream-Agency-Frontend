<template>
  <div class="main-container flex flex-row justify-between items-center">
    <div class="buttons flex flex-col justify-end h-full mr-12">
      <div class="flex flex-row justify-between">
        <div class="backward mr-1 w-11 h-11" @click="goBackward"></div>
        <div class="forward ml-1 w-11 h-11" @click="goForward"></div>
      </div>
    </div>
    <div ref="swiper" class="swiper">
      <!-- Additional required wrapper -->
      <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide" v-for="(slide, index) in slides" :key="index">
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
        </div>
      </div>
      <!-- If we need pagination -->
    </div>
  </div>
</template>

<script>
// import Swiper core and required modules
import Swiper, { Navigation, Pagination } from 'swiper'
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
export default {
  name: 'CardComponent',

  mounted() {
    this.initSwiper()
    window.addEventListener('resize', this.handleResize)
  },

  beforeDestroy() {
    window.removeEventListener('resize', this.handleResize)
  },
  data() {
    return {
      menuOpen: false,
      swiper: null,
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
    initSwiper() {
      this.swiper = new Swiper(this.$refs.swiper, {
        modules: [Navigation, Pagination],
        loop: true,

        slidesPerView: this.getSlidesPerView(),
        spaceBetween: 150,
      })
    },
    goForward() {
      if (this.swiper) {
        this.swiper.slideNext()
        console.log('hello')
      }
    },

    goBackward() {
      if (this.swiper) {
        this.swiper.slidePrev()
      }
    },
    getSlidesPerView() {
      // Adjust slides per view based on screen size
      if (window.innerWidth < 576) {
        return 1
      } else if (window.innerWidth < 1110) {
        return 2
      } else if (window.innerWidth < 1495) {
        return 3
      } else {
        return 4
      }
    },
  },
}
</script>

<style scoped>
.forward {
  border: 1px solid black;
  border-radius: 9999px;
  background-image: url(../assets/icons/backward.png);
  background-repeat: no-repeat;
  background-position: center;
  background-size: auto;
}
.backward {
  border: 1px solid black;
  border-radius: 9999px;
  background-image: url(../assets/icons/backward.png);
  background-repeat: no-repeat;
  background-position: center;
  background-size: auto;
  transform: scaleX(-1);
}

.box .rectangle {
  background: white;
  width: 300px;
  height: 170px;
  border-radius: 20px;
  box-shadow: 0px 0px 9px 2px rgba(0, 0, 0, 0.05);
  padding: 10px 10px 10px 10px;
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
  .box .rectangle {
    display: flex;
    flex-direction: column;
    background: white;
    width: 100%;
    height: 100%;
    padding: 15px 15px 13px 15px;
  }

  .buttons {
    height: 20%;
    margin: 5px;
  }
  .main-container {
    flex-direction: column;
    justify-content: center;
    align-items: center;
    display: flex;

    margin-right: 14px;
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
}
</style>
