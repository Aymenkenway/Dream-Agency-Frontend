<template>
  <div class="aboutus-container flex flex-row justify-between">
    <div class="left-hero flex flex-row justify-evenly flex-1 items-center">
      <img class="overlay-image" src="../assets/icons/hero2.png" alt="" />
    </div>
    <div
      class="right-hero flex flex-row justify-between flex-1 items-center ml-10"
    >
      <div>
        <div class="titles">
          <span class="we-help-you">Abous Us<br /></span
          ><span class="grow-business">Fake or Real</span>
        </div>
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
        <div class="button-container">
          <Button class="w-52 h-14" />
        </div>
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

.grow-business {
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
@media (max-width: 768px) {
  .lorem {
    width: 100%;
  }
  .aboutus-container {
    flex-direction: row;
  }
  .we-help-you {
    font-size: 40px;
  }
  .grow-business {
    font-size: 40px;
  }
}

@media (max-width: 520px) {
  .grow-business {
    margin-top: 0;
    padding: 0;
  }
  .we-help-you {
    margin: 0;
    padding: 0;
  }
  .overlay-image {
    display: none;
  }
  .right-hero {
    align-items: center;
    width: 80%;
    margin: 0;
  }

  .aboutus-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 0;
  }
  .titles {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding-bottom: 30px;
  }
  .button-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 30px;
  }
  .lorem {
    padding: 0;
  }
}
</style>
