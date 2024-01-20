<template>
  <div class="footer-contain flex flex-row justify-between">
    <div class="w-1/3 h-1/2 mt-16">
      <div
        class="quote-container flex flex-col justify-between items-start ml-10 p-6"
      >
        <h1 class="dream-agency">Dream Agency</h1>
        <p class="paragraph my-4">
          Lorem Ipsum has been the industry's standard dummy text ever since the
          1500s, when an unknown printer took a galley of type and scrambled it
          to make a type specimen book. It has survived not only five centuries.
        </p>
        <div class="flex flex-row items-center my-4">
          <p class="author">GET IN TOUCH</p>
        </div>
        <div
          class="flex flex-row border w-full h-12 justify-between items-center"
        >
          <div class="email bg-black h-full flex flex-col justify-center pl-4">
            <p>ENTER YOUR EMAIL</p>
          </div>

          <div
            class="send w-1/3 h-full bg-white flex flex-col justify-center items-center"
          >
            <p>SEND</p>
          </div>
        </div>
      </div>
    </div>
    <div class="w-1/3 mt-16 mr-32">
      <div>
        <MapComponent />
      </div>
    </div>
  </div>
</template>

<script>
import MapComponent from '../components/Map.vue'
export default {
  name: 'FooterView',
  components: {
    MapComponent,
    // added
  },
}
</script>

<style scoped>
.footer-contain {
  background-color: black;
  border-top-right-radius: 158px;
  padding-bottom: 15px;
}
.paragraph {
  color: white;
  font-size: 16px;
  font-family: Hind Vadodara;
  font-weight: 400;
  line-height: 25.49px;
  letter-spacing: 0.32px;
  word-wrap: break-word;
}
.author {
  color: white;
  font-size: 16px;
  font-family: Hind Vadodara;
  font-weight: 600;
  text-transform: uppercase;
  line-height: 25.49px;
  letter-spacing: 0.32px;
  word-wrap: break-word;
}

.quote-container {
  width: 100%;
  box-shadow: 0px 0px 7px 1px rgba(0, 0, 0, 0.08);
  align-items: left;
}
.dream-agency {
  color: white;
  font-size: 36px;
  font-family: Playfair Display;
  font-weight: 700;
  letter-spacing: 0.36px;
  word-wrap: break-word;
}
.email {
  width: 100%;
  height: 100%;
  border: 1px white solid;
}
.email p {
  color: white;
  font-size: 16px;
  font-family: Hind Vadodara;
  font-weight: 400;
  text-transform: uppercase;
  line-height: 25.49px;
  letter-spacing: 0.32px;
  word-wrap: break-word;
}
.send p {
  color: black;
  font-size: 16px;
  font-family: Hind Vadodara;
  font-weight: 600;
  text-transform: uppercase;
  line-height: 25.49px;
  letter-spacing: 0.32px;
  word-wrap: break-word;
}
</style>
