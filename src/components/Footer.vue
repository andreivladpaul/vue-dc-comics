<template>
    
        <footer>
            <div class="footer-top">
                <div class="layout">
                   <!--  <img :src="require(../assets/${icon.url + icon.path + icon.extension})" :alt="icon.path"> -->
                </div>
            </div>
            <div class="footer-medium">
                <div class="layout">

                </div>
            </div>
            <div class="footer-bottom">
                <div class="layout">

                </div>
            </div>

        </footer>
    
    
</template>

<script>
 export default {
     name: 'Footer',
     data() {
         return{
             links: [
                 {
                     text: 'characters',
                     url: '#',
                     current: false
                 },
                 {
                     text: 'comics',
                     url: '#',
                     current: true
                 },
                 {
                     text: 'movies',
                     url: '#',
                     current: false
                 },
                 {
                     text: 'tv',
                     url: '#',
                     current: false
                 },
                 {
                     text: 'games',
                     url: '#',
                     current: false
                 },
                 {
                     text: 'collectibles',
                     url: '#',
                     current: false
                 },
                 {
                     text: 'videos',
                     url: '#',
                     current: false
                 },
                 {
                     text: 'fans',
                     url: '#',
                     current: false
                 },
                 {
                     text: 'news',
                     url: '#',
                     current: false
                 },
                 {
                     text: 'shop',
                     url: '#',
                     current: false
                 }
             ]
         }
     }
 }
</script>

<style scoped lang="scss">
@import '../style/vars';

footer {

    .footer-top{
        background-color: $blue;
        height: 150px;
    }

    .footer-medium {
    height: 370px;
    background-image: url(~@/assets/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    }

    .footer-bottom {
        background-color: $grey;
        height: 110px;
    }
    
}



</style>