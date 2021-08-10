<template>
  <div class="container">
    <h2 class="title">Propiedades destacadas</h2>
    <div class="sliderSection">
      <Slider/>
    </div>
  </div>
</template>

<script>
import Slider from '@/components/Slider.vue'

export default {
  name: 'BannerTwo',

  components: {
    Slider
  }
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  height: 650px;
  background: #fff;
  margin: 10px 0;

  .title {
    font-size: 2.4rem;
    text-transform: uppercase;
    color: #786d69;
    margin-top: 20px;
  }
}
</style>
