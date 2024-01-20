<template>
  <div class="aboutus-container flex flex-row justify-between">
    <div class="left-hero flex flex-row justify-evenly flex-1 items-center">
      <img class="overlay-image" src="../assets/icons/hero2.png" alt="" />
    </div>
    <div
      class="right-hero flex flex-row justify-between flex-1 items-center ml-10"
    >
      <div>
        <p>
          <span class="we-help-you">Abous Us</span>
          <br />
          <span class="grow-businnes">Fake or Real</span>
        </p>
        <p class="lorem w-9/12 mb-3 pt-4">
          Lorem Ipsum has been the industry's standard dummy text ever since the
          1500s, when an unknown printer took a galley of type and scrambled it
          to make a type specimen book.
        </p>

        <p class="lorem w-9/12 pb-8">
          Lorem Ipsum has been the industry's standard dummy text ever since the
          1500s, when an unknown printer took a galley of type and scrambled it
          to make a type specimen book.
        </p>
        <Button class="w-52 h-14" />
      </div>
    </div>
  </div>
</template>

<script>
import Button from '../components/Button.vue'
export default {
  name: 'AboutUs',
  components: { Button },
}
</script>

<style scoped>
.we-help-you {
  color: #331b3b;
  font-size: 48px;
  font-family: Hind Vadodara;
  font-weight: 700;
  line-height: 51.02px;
  word-wrap: break-word;
}

.grow-businnes {
  color: #331b3b;
  font-size: 48px;
  font-family: Hind Vadodara;
  font-weight: 300;
  line-height: 51.02px;
  word-wrap: break-word;
}
.lorem {
  color: rgba(51, 27, 59, 0.66);
  font-size: 17px;
  font-family: 'Hind Vadodara' sans-serif;
  font-weight: 400;
  line-height: 24.87px;
  letter-spacing: 0.34px;
  word-wrap: break-word;
}

.overlay-image {
  max-width: 100%;
}
</style>
