<template>
  <section class="mt-24 bg-cyan py-12 dark:bg-[#6FC2C5]">
    <h2
      class="font-medium text-center text-2xl leading-normal text-white lg:text-5xl lg:leading-[60px]"
    >
      We Are Loved By Users<br />
      And Clients Worldwide
    </h2>

    <div class="mx-auto mt-12 flex w-5/6 items-center justify-between lg:w-3/4">
      <div ref="swiper" class="swiper pb-16">
        <!-- Additional required wrapper -->
        <div class="swiper-wrapper">
          <!-- Slides -->
          <div
            style="width: 696px; margin-right: 48px"
            class="swiper-slide"
            v-for="(slide, index) in slides"
            :key="index"
          >
            <div
              class="flex h-[350px] flex-col rounded-br-[30px] justify-between rounded-bl-[30px] rounded-tl-[30px] bg-white p-8 xl:p-14"
            >
              <p class="text-lg font-normal text-[#151517] lg:text-xl">
                {{ slide.comment }}
              </p>
              <div
                class="mt-8 flex flex-col justify-between gap-4 xl:mt-16 xl:flex-row xl:items-center xl:gap-0"
              >
                <div class="flex gap-5">
                  <img :src="slide.image" alt="Ronald Richards picture" />
                  <div>
                    <p class="text-base font-semibold">
                      {{ slide.author }}
                    </p>
                    <p class="text-sm leading-6 dark:text-lightGrey">
                      {{ slide.role }}
                    </p>
                  </div>
                </div>
                <div class="flex items-center justify-center gap-2">
                  {{ slide.rating }}
                  <div class="flex items-center gap-1">
                    <svg
                      stroke="currentColor"
                      fill="#F5BF75"
                      stroke-width="0"
                      viewBox="0 0 16 16"
                      height="18"
                      width="18"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M3.612 15.443c-.386.198-.824-.149-.746-.592l.83-4.73L.173 6.765c-.329-.314-.158-.888.283-.95l4.898-.696L7.538.792c.197-.39.73-.39.927 0l2.184 4.327 4.898.696c.441.062.612.636.282.95l-3.522 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256z"
                      ></path></svg
                    ><svg
                      stroke="currentColor"
                      fill="#F5BF75"
                      stroke-width="0"
                      viewBox="0 0 16 16"
                      height="18"
                      width="18"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M3.612 15.443c-.386.198-.824-.149-.746-.592l.83-4.73L.173 6.765c-.329-.314-.158-.888.283-.95l4.898-.696L7.538.792c.197-.39.73-.39.927 0l2.184 4.327 4.898.696c.441.062.612.636.282.95l-3.522 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256z"
                      ></path></svg
                    ><svg
                      stroke="currentColor"
                      fill="#F5BF75"
                      stroke-width="0"
                      viewBox="0 0 16 16"
                      height="18"
                      width="18"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M3.612 15.443c-.386.198-.824-.149-.746-.592l.83-4.73L.173 6.765c-.329-.314-.158-.888.283-.95l4.898-.696L7.538.792c.197-.39.73-.39.927 0l2.184 4.327 4.898.696c.441.062.612.636.282.95l-3.522 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256z"
                      ></path></svg
                    ><svg
                      stroke="currentColor"
                      fill="#F5BF75"
                      stroke-width="0"
                      viewBox="0 0 16 16"
                      height="18"
                      width="18"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M3.612 15.443c-.386.198-.824-.149-.746-.592l.83-4.73L.173 6.765c-.329-.314-.158-.888.283-.95l4.898-.696L7.538.792c.197-.39.73-.39.927 0l2.184 4.327 4.898.696c.441.062.612.636.282.95l-3.522 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256z"
                      ></path></svg
                    ><svg
                      stroke="currentColor"
                      fill="#F5BF75"
                      stroke-width="0"
                      viewBox="0 0 16 16"
                      height="18"
                      width="18"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M5.354 5.119 7.538.792A.516.516 0 0 1 8 .5c.183 0 .366.097.465.292l2.184 4.327 4.898.696A.537.537 0 0 1 16 6.32a.548.548 0 0 1-.17.445l-3.523 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256a.52.52 0 0 1-.146.05c-.342.06-.668-.254-.6-.642l.83-4.73L.173 6.765a.55.55 0 0 1-.172-.403.58.58 0 0 1 .085-.302.513.513 0 0 1 .37-.245l4.898-.696zM8 12.027a.5.5 0 0 1 .232.056l3.686 1.894-.694-3.957a.565.565 0 0 1 .162-.505l2.907-2.77-4.052-.576a.525.525 0 0 1-.393-.288L8.001 2.223 8 2.226v9.8z"
                      ></path>
                    </svg>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- If we need pagination -->
      </div>
    </div>
  </section>
</template>

<script>
import Swiper, { Navigation, Pagination, Autoplay } from 'swiper'
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import 'swiper/css/autoplay'
export default {
  name: 'FeedbacksView',
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
          author: 'Ronald Richards',
          role: ' UI/UX Designer',
          comment:
            '  One of the best additions to our feedback loop has been the company-wide adoption of Fellow.',
          image: require('../assets/icons/pp1.png'),
          rating: '4.5',
        },
        {
          author: 'Ronald Richards',
          role: ' UI/UX Designer',
          comment:
            '  It provides an amazing platform for constant conversations and direct feedback between managers and direct reports.',
          image: require('../assets/icons/pp2.png'),
          rating: '4.5',
        },
        {
          author: 'Ronald Richards',
          role: ' UI/UX Designer',
          comment:
            '  It provides an amazing platform for constant conversations and direct feedback between managers and direct reports.',
          image: require('../assets/icons/pp2.png'),
          rating: '4.5',
        },
      ],
    }
  },
  methods: {
    initSwiper() {
      this.swiper = new Swiper(this.$refs.swiper, {
        modules: [Navigation, Pagination, Autoplay],

        loop: true,
        autoplay: {
          delay: 2000, // Set the delay between slides in milliseconds (e.g., 5000 for 5 seconds)
          disableOnInteraction: false, // Allow navigation while autoplay is active
        },
        slidesPerView: this.getSlidesPerView(),
        spaceBetween: 40,
      })
    },
    handleResize() {
      if (this.swiper) {
        this.swiper.destroy() // Destroy the existing Swiper instance
        this.initSwiper() // Reinitialize Swiper with updated configuration
      }
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
      if (window.innerWidth < 800) {
        return 1
      } else if (window.innerWidth < 1495) {
        return 2
      } else {
        return 2
      }
    },
  },
}
</script>

<style scoped></style>
