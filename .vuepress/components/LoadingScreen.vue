<template>
  <div v-if="loader" id="loading">
    <img class="img" src="/loading.gif" alt="loading..." />
  </div>
</template>

<script>
export default {
  name: "Loading",
  data() {
    return {
      loader: true,
    };
  },
  mounted() {
    setTimeout(() => {
      this.loader = false;
    }, 1700);
  },
};
</script>

<style>
#loading {
  margin-top: 0;
  position: absolute;
  z-index: 1000;
  background-color: rgba(255, 255, 255, 0.884);
  height: 100vh;
  width: 100vw;
}
.img {
  position: relative;
  margin-left: 12%;
  margin-top: 5%;
  width: 200px;
}
</style>