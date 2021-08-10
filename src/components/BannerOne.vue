<template>
  <div class="container">
    <div class="container-vignete">
      <h1 class="title">Brücken</h1>
      <a href="#" class="btn">Conocer más</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BannerOne'
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  height: 100vh;
  background-image: url('../assets/01.jpg');
  mask-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  z-index: 2;
  position: relative;

  &-vignete {
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background: rgba($color: #000, $alpha: 0.4);
    position: relative;
    z-index: 1;

    .title {
      font-size: 5rem;
      color: #fff;
      margin-bottom: 30px;
    }

    .btn {
      color: #fff;
      font-size: 1.1rem;
      line-height: 1.5;
      font-weight: bold;
      text-transform: uppercase;
      background: #a5d7d5;
      padding: 10px 35px;
      border-radius: 5px;
      text-decoration: none;
    }

    .btn:hover {
      background: #a2efdf;
    }
  }
}
</style>
