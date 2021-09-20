<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />

    
  </div>
</template>

<script>
import Header from '../src/components/Header.vue'
import Main from '../src/components/Main.vue'
import Footer from '../src/components/Footer.vue'

import '@/style/generals.scss'



export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>


<style lang="scss">
@import '@/style/generals.scss'

</style>
