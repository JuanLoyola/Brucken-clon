<template>
  <div class="container">
    <div class="container-vignete">
      <h1 class="title"><span>Brücken</span></h1>
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
      display: inline-block;
      overflow: hidden;
      clear: both;
      position: relative;
    }

    .title span {
      color: transparent;
      -webkit-animation: show 0s forwards 0.4s;
      animation: show 0s forwards 0.4s;
    }
    .title:after {
      content: '';
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      background: white;
      -webkit-transform: translate3d(110%, 0, 0);
      transform: translate3d(110%, 0, 0);
      -webkit-animation: left-to-right 1s cubic-bezier(.17,.67,.83,.67);
      animation: left-to-right 1s cubic-bezier(.17,.67,.83,.67);
    }

    @-webkit-keyframes show {
      0% {
        color: transparent;
      }
      100% {
        color: white;
      }
    }
    @keyframes show {
      0% {
        color: transparent;
      }
      100% {
        color: white;
      }
    }

    /* Left-to-right animation */
    @-webkit-keyframes left-to-right {
      0% {
        -webkit-transform: translate3d(-100%, 0, 0);
      }
      100% {
        -webkit-transform: translate3d(110%, 0, 0);
      }
    }
    @keyframes left-to-right {
      0% {
        transform: translate3d(-100%, 0, 0);
      }
      100% {
        transform: translate3d(110%, 0, 0);
      }
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
