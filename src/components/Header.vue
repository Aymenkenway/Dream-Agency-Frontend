<template>
  <nav
    class="nav mx-auto flex w-5/6 max-w-6xl items-center justify-between py-10 lg:w-3/4"
  >
    <a class="text-xl font-bold" href="/">Ariene Rey</a>

    <ul v-if="!showHamburger" class="flex items-center justify-between gap-10">
      <li class="font-bold text-yellow-500">Home</li>
      <li class="font-medium">About</li>
      <li class="font-medium">Projects</li>
      <li class="font-medium">Contact</li>
    </ul>

    <div v-if="showHamburger">
      <Bubble disableEsc class="bm-burger-button">
        <li>Home</li>
        <li>About</li>
        <li>Projects</li>
        <li>Contact</li>
      </Bubble>
    </div>
  </nav>
</template>

<script>
import { Bubble } from 'vue-burger-menu'
export default {
  name: 'HeaderComponent',
  components: { Bubble },
  data() {
    return {
      showHamburger: false,
    }
  },
  mounted() {
    this.checkScreenWidth()
    window.addEventListener('resize', this.checkScreenWidth)
  },
  beforeDestroy() {
    window.removeEventListener('resize', this.checkScreenWidth)
  },
  methods: {
    checkScreenWidth() {
      this.showHamburger = window.innerWidth <= 1030
    },
  },
}
</script>

<style scoped>
@media (max-width: 1030px) {
  .nav {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
  }
  .bm-burger-button {
    left: 0;
    top: 0;
    cursor: pointer;
  }
}
</style>
