<template>
  <div class="home">
    <BannerOne />
    <SearchBox />
    <BannerTwo />
    <Footer />
  </div>
</template>

<script>
import BannerOne from '@/components/BannerOne.vue'
import SearchBox from '@/components/SearchBox.vue'
import BannerTwo from '@/components/BannerTwo.vue'
import Footer from '@/components/Footer.vue'
export default {
  name: 'Home',
  components: {
    BannerOne,
    SearchBox,
    BannerTwo,
    Footer
  }
}
</script>
