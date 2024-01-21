<template>
  <div class="hero-container flex flex-row justify-between">
    <div
      class="right-hero flex flex-row justify-between flex-1 items-center ml-10"
    >
      <div class="left-hero-container">
        <p>
          <span class="we-help-you">We Help you</span>

          <span class="grow-business"
            ><p class="to-grow">to grow your</p>
            <p class="business">Business</p></span
          >
        </p>

        <p class="lorem w-9/12 pt-8 pb-8">
          Lorem Ipsum has been the industry&#39;s standard dummy text ever since
          the 1500s, when an unknown printer took a galley of type and scrambled
          it to make a type specimen book.
        </p>
        <Button class="w-52 h-14" />
      </div>
    </div>

    <div class="left-hero flex flex-row justify-evenly flex-1 items-center">
      <img src="../assets/icons/Vector2.png" alt="" />
      <img
        class="absolute overlay-image"
        src="../assets/icons/people2.png"
        alt=""
      />
    </div>
  </div>
</template>

<script>
import Button from '../components/Button.vue'
export default {
  name: 'HeroView',
  components: { Button },
}
</script>

<style scoped>
.we-help-you {
  color: #331b3b;
  font-size: 87px;
  font-family: 'Hind Vadodara' sans-serif;
  font-weight: 700;
  line-height: 90px;
}

.grow-business {
  color: #331b3b;
  font-size: 87px;
  font-family: 'Hind Vadodara' sans-serif;
  font-weight: 300;
  line-height: 90px;
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
  max-width: 55%;
  margin-right: 8%;
}

/* here screen */
@media (max-width: 768px) {
  .we-help-you,
  .grow-business {
    font-size: 40px; /* Adjust font size for smaller screens */
    line-height: 55px; /* Adjust line height for smaller screens */
  }

  .lorem {
    font-size: 14px; /* Adjust font size for smaller screens */
    line-height: 20px; /* Adjust line height for smaller screens */
  }
}

@media (max-width: 590px) {
  .left-hero {
    display: none;
  }
  .right-hero {
    margin-left: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .left-hero-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .grow-business {
    font-size: 40px; /* Adjust font size for smaller screens */
    line-height: 55px; /* Adjust line height for smaller screens */
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .we-help-you {
    font-size: 20px;
  }
  .lorem {
    font-size: 14px; /* Adjust font size for smaller screens */
    line-height: 20px; /* Adjust line height for smaller screens */
    align-items: center;
    padding-top: 20px;
  }
}
@media (max-width: 1030px) {
  .we-help-you,
  .grow-business {
    font-size: 50px; /* Adjust font size for smaller screens */
    line-height: 80px; /* Adjust line height for smaller screens */
  }
}
</style>
