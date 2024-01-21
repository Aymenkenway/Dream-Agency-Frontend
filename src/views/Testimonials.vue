<template>
  <div class="testi-container flex flex-col justify-center items-center">
    <div class="content pb-12 flex flex-col items-center">
      <span class="what-we-do">Our Testimonials<br /></span
      ><span class="for-you-business"
        >What Our Clients<span>Are Saying</span></span
      >
    </div>
    <div class="q-container w-3/5 flex flex-row">
      <div
        class="quote-container flex flex-col justify-between border items-start mr-8 p-6"
      >
        <img class="image" src="../assets/icons/quote.png" alt="" />
        <p class="paragraph py-4">
          Lorem Ipsum has been the industry's standard dummy text ever since the
          1500s, when an unknown printer took a galley of type and scrambled it
          to make a type specimen book. It has survived not only five centuries.
        </p>
        <div class="flex flex-row items-center">
          <img
            class="author-vector mr-2"
            src="../assets/icons/quote-vector.png"
            alt=""
          />
          <p class="author">Ui Soup</p>
        </div>
      </div>
      <div
        class="quote-container flex flex-col justify-between items-start ml-8 p-6"
      >
        <img class="image" src="../assets/icons/quote.png" alt="" />
        <p class="paragraph py-4">
          Lorem Ipsum has been the industry's standard dummy text ever since the
          1500s, when an unknown printer took a galley of type and scrambled it
          to make a type specimen book. It has survived not only five centuries.
        </p>
        <div class="flex flex-row items-center">
          <img
            class="author-vector mr-2"
            src="../assets/icons/quote-vector.png"
            alt=""
          />
          <p class="author">Ui Soup</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TestimonialsView',
}
</script>

<style scoped>
.testi-container {
  height: 500px;
}
.what-we-do {
  color: #331b3b;
  font-size: 48px;
  font-family: 'Hind Vadodara', sans-serif;
  font-weight: 700;
  line-height: 53.18px;
  word-wrap: break-word;
}

.for-you-business {
  color: #331b3b;
  font-size: 48px;
  font-family: 'Hind Vadodara', sans-serif;
  font-weight: 300;
  line-height: 53.18px;
  word-wrap: break-word;
}
.image {
  width: 44.8px;
  height: 39.18px;
}
.paragraph {
  color: #331b3b;
  font-size: 16px;
  font-family: Hind Vadodara;
  font-weight: 400;
  line-height: 25.49px;
  letter-spacing: 0.32px;
  word-wrap: break-word;
}
.author {
  color: black;
  font-size: 16px;
  font-family: Hind Vadodara;
  font-weight: 600;
  line-height: 25.49px;
  letter-spacing: 0.32px;
  word-wrap: break-word;
}
.author-vector {
  width: 10px;
  height: 5px;
}
.quote-container {
  width: 100%;
  height: 100%;
  background: white;
  box-shadow: 0px 0px 7px 1px rgba(0, 0, 0, 0.08);
  align-items: left;
}
@media (max-width: 1037px) {
  .testi-container {
    margin-top: 30px;
  }
  .q-container {
    width: 90%;
  }
  .what-we-do {
    font-size: 40px;
  }
  .for-you-business {
    font-size: 40px;
  }
}

@media (max-width: 590px) {
  .testi-container {
    margin-top: 200px;
  }
  .content {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding-bottom: 30px;
  }
  .for-you-business {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .q-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 80%;
  }
  .quote-container {
    margin: 0;
    margin-top: 10px;
  }
}
</style>
