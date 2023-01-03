<template>
  <v-row class="main-row" justify="center" align="center">
    <div class="main-img">
      <img src="~/assets/images/projects/crops/pic5.jpg" width="100%" />
    </div>
    <div class="main-text">
      <h2>Quality Custom Home Building</h2>
    </div>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style scoped>
@import "~/assets/styles.css";

.main-row {
  margin-top: 1px;
}

.main-img {
  filter: blur(3px);
}

.main-text {
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0, 0.4); /* Black w/opacity/see-through */
  color: #edf0ee;
  font-weight: bold;
  border: 3px solid #f1f1f1;
  border-radius: 2px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
  width: 80%;
  padding: 20px;
  text-align: center;
}

</style>