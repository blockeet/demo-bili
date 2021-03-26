<template>
  <div class="banner">
    <div class="logo">
      <a href="/" class="head-logo">
        <img src="../../public/images/bililogo.png" alt="">
      </a>
    </div>
  </div>
</template>

<style lang="scss">
.banner {
  margin: 0 auto;
  position: relative;
  z-index: 0;
  min-height: 155px;
  height: 9.375vw;
  min-width: 999px;
  background-color: #f9f9f9;
  display: flex;
  justify-content: center;
  background-image: url('../../public/images/banner.png');
  background-repeat: no-repeat;
  background-position: center 0;
  background-size: cover;
  .logo {
    position: relative;
    width: 1414px;
    margin: 0;
    .head-logo {
      position: absolute;
      width: 220px;
      height: 50%;
      min-height: 60px;
      bottom: 10px;
      z-index: 1;
      left: 0;
      img {
        height: 100%;
      }
    }
  }
}
</style>

<script>
export default {
  name: 'NavBanner'
}
</script>
