<template>
    <div class="banner">
        <div class="container">
            <div class="icon" v-for="(icon, index) in icons" :key="index">
                <img :src="require(`../assets/${icon.url + icon.path + icon.extension}`)" :alt="icon.text">
                <h3>{{icon.text.toUpperCase()}}</h3>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'BannerFeatures',

    data() {
        return {
            icons: [
                {   
                    url: 'img/buy-comics-',
                    path: 'digital-comics',
                    extension: '.png',
                    text: 'Digital Comics'
                },
                {   
                    url: 'img/buy-comics-',
                    path: 'merchandise',
                    extension: '.png',
                    text: 'DC Merchandise'
                },
                {   
                    url: 'img/buy-comics-',
                    path: 'subscriptions',
                    extension: '.png',
                    text: 'Subscriptions'
                },
                {   
                    url: 'img/buy-comics-',
                    path: 'shop-locator',
                    extension: '.png',
                    text: 'Shop Locator'
                },
                {   
                    url: 'img/buy-dc-',
                    path: 'power-visa',
                    extension: '.svg',
                    text: 'Power Visa'
                },
            ]
        }
    }
}

</script>

<style scoped lang="scss">
@import "../style/general";

.banner {
    background-color: $primary-color;
    height: 200px;

    .container{
        @include center(vertical);
        justify-content: space-around;
        
    }
}

.icon {
    height: 50px;
    @include center(vertical);
    cursor: pointer;    

    h3{font-size: $fs-s; color: $txt-light; font-weight: $light; margin-left: 10px;}
    img{height: 100%; max-width: 60px;}


}

</style>