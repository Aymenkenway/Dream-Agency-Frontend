<template>
  <div
    class="main-container flex flex-row justify-between items-center md:items-end"
  >
    <div class="buttons flex flex-col justify-end h-full mr-12">
      <div class="btns flex flex-row">
        <div class="backward mr-3 w-11 h-11" @click="goBackward"></div>
        <div class="forward ml-3 w-11 h-11" @click="goForward"></div>
      </div>
    </div>
    <div ref="swiper" class="swiper">
      <!-- Additional required wrapper -->
      <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide" v-for="(slide, index) in slides" :key="index">
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
  name: 'SecondCardComponent',

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

<style lang="scss" scoped>
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
.box {
  padding: 10px 10px 0px 10px;
  display: flex;
  flex-direction: row;
  background-color: #fff;
  border-radius: 3%;
  justify-content: center;
  width: 300px;
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
@media (max-width: 767px) {
  .view {
    font-size: 8px;
  }

  .box .rectangle {
    width: 100%; /* Full width on smaller screens */
  }
  .title {
    font-size: 12px;
  }
}

@media (max-width: 590px) {
  .box .rectangle {
    width: 100%;
  }
  .btns {
    margin-left: 20px;
  }
  .buttons {
    width: 30%;
  }
  .backward {
    margin-right: 2px;
  }
  .forward {
    margin-left: 10px;
  }
  .box {
    width: 99%;
    height: 300px;
  }
}
</style>
