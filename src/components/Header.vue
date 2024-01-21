<template>
  <div class="main-container flex flex-row items-stretch justify-between">
    <ul
      v-if="!showHamburger"
      class="links flex flex-row justify-evenly flex-1 items-center ml-2"
    >
      <li>Home</li>
      <li>About US</li>
      <li>Services</li>
      <li>Contact Us</li>
    </ul>
    <div
      v-if="showHamburger"
      class="humburger flex flex-row justify-evenly flex-1 items-center"
    >
      <ScaleRotate disableEsc>
        <li>Home</li>
        <li>About US</li>
        <li>Services</li>
        <li>Contact Us</li>
        <li>Facebook</li>
        <li>LinkedIn</li>
        <li>Instagram</li>
      </ScaleRotate>
    </div>

    <div class="brand flex flex-row justify-evenly flex-1 items-center">
      <h1>Dream Agency</h1>
    </div>

    <div
      v-if="!showHamburger"
      class="icons flex flex-row justify-end gap-4 flex-1 mr-14"
    >
      <div class="icons-border flex flex-row justify-center">
        <img class="icon" src="../assets/icons/facebook.png" alt="Facebook" />
      </div>
      <div class="icons-border flex flex-row justify-center">
        <img class="icon" src="../assets/icons/linkedin.svg" alt="LinkedIn" />
      </div>
      <div class="icons-border flex flex-row justify-center">
        <img class="icon" src="../assets/icons/instagram.svg" alt="Instagram" />
      </div>
    </div>
  </div>
</template>

<script>
import { ScaleRotate } from 'vue-burger-menu'
export default {
  name: 'HeaderComponent',
  components: { ScaleRotate },
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
.icons-border img {
  width: 20px;
  height: 30px;
  transform: rotate(330deg);
}
.icons-border {
  align-items: center;
  width: 43.614px;
  height: 49.614px;
  transform: rotate(30.5deg);
  border: 2px rgba(51, 27, 59, 0.64) solid;
  border-radius: 60%;
}

.brand {
  color: #331b3b;
  font-size: 24px;
  font-family: 'Playfair Display';
  font-weight: 700;
  letter-spacing: 0.24px;
  padding-left: 7%;
}
.links {
  color: #331b3b;

  font-family: 'Hind Vadodara' sans-serif;
  letter-spacing: 0.16px;
}
@media (max-width: 930px) {
  .links {
    font-size: 14px;
    flex: 100px;
  }
}
@media (max-width: 864px) {
  .links {
    font-size: 13px;
    flex: 100px;
  }
  .brand {
    font-size: 20px;
    padding: 0;
  }
}
@media (max-width: 755px) {
  .links {
    font-size: 12px;
    flex: 100px;
  }
  .brand {
    font-size: 20px;
    padding: 0;
  }
}
@media (max-width: 688px) {
  .brand {
    font-size: 20px;
    padding: 0;
  }
  .icons {
    width: 90px;
    margin-right: 10px;
  }
}

@media (max-width: 580px) {
  .main-container {
    justify-content: space-between;
  }
  .brand {
    font-size: 18px;
    padding: 0;
  }

  .icons {
    width: 90px;
    margin-right: 10px;
  }
}
@media (max-width: 590px) {
  .main-container {
    display: flex;
    justify-content: space-between;
    margin-right: 30px;
  }
  .brand {
    font-size: 12px;
    padding: 0;
    margin-left: 20%;
    display: flex;
    justify-content: start;
  }
  .icons-border {
    align-items: center;
    width: 20.614px;
    height: 26.614px;
    transform: rotate(30.5deg);
    border: 2px rgba(51, 27, 59, 0.64) solid;
    border-radius: 60%;
  }
  .icons-border img {
    width: 11px;
    height: 12px;
    transform: rotate(330deg);
  }
  .links {
    font-size: 9px;
    flex: 100px;
  }
  .brand {
    display: flex;
    align-items: end;
    justify-content: end;
    align-items: end;
    font-size: 17px;
  }
}
@media (max-width: 1030px) {
  .brand {
    font-size: 30px;
    padding: 0;
    justify-content: center;
    flex: 100%;
  }
}
</style>
