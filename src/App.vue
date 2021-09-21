<template>
  <div id="app">
    <Header/>
    <Products/>
    <BannerFeatures/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Products from './components/Products.vue'
import BannerFeatures from './components/BannerFeatures.vue'
import Footer from './components/Footer.vue'


export default {
  name: 'App',
  components: {
    Header,
    Products,
    Footer,
    BannerFeatures
  }
}
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
  @import '@/style/general.scss';
</style>