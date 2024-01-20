<template>
  <div class="flex flex-row items-stretch justify-between">
    <ul class="links flex flex-row justify-evenly flex-1 items-center ml-2">
      <li>Home</li>
      <li>About US</li>
      <li>Services</li>
      <li>Contact Us</li>
    </ul>

    <div class="brand flex flex-row justify-evenly flex-1 items-center">
      <h1>Dream Agency</h1>
    </div>

    <div class="flex flex-row justify-end gap-4 flex-1 mr-14">
      <div class="icons-border flex flex-row justify-center">
        <img src="../assets/icons/facebook.png" alt="Facebook" />
      </div>
      <div class="icons-border flex flex-row justify-center">
        <img src="../assets/icons/linkedin.svg" alt="LinkedIn" />
      </div>
      <div class="icons-border flex flex-row justify-center">
        <img src="../assets/icons/instagram.svg" alt="Instagram" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderComponent',
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
</style>
