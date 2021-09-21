<template>
    <div class="my-content">
        <div class="jumbotron">
            <img src="@/assets/img/jumbotron.jpg" alt="jumbotron">
        </div>

        <div class="container clearfix">
            <div class="current-series">
                <span class="section-title">CURRENT SERIES</span>
            </div>
            <!-- COMICS -->
            <div class="dc-products clearfix">
                    <ProductCard 
                        v-for="(product, index) in products"
                        :key="index"
                        :prod="product"
                    />
                
            </div>

            <div class="btn-sec">
                <button>LOAD MORE</button>
            </div>
            
        </div>
        
    </div>
</template>

<script>
import ProdItems from '@/assets/data/DCComics.js'
import ProductCard from '@/components/ProductCard.vue'
export default {
    name: 'Products',
    components: {
        ProductCard,
    },
    data(){
        return{
            products: ProdItems,
        }
    }
}
</script>

<style scoped lang="scss">
@import '@/style/general.scss';

.my-content{
    background-color: $secondary-color;

    /* .container {
        @include center(both);
    } */
    
    .jumbotron{
        height: 350px;

        img{
            height: 100%;
            width: 100%;
            object-position: top;
            object-fit: cover
        };
    }

    .current-series{
        position: absolute;
        top: -20px;
        left: 40px;
        display: inline-block;
        height: 40px;
        width: max-content;
        background-color: $primary-color;
        padding: 8px 15px;
        color: $txt-light;
        font-size: $fs-lg;
    }

    .dc-products{
        text-align: center;
        padding: 50px 90px;
 
    }
    
    .btn-sec{
        @include center(both);

        button {
            background-color: $primary-color;
            padding: 10px 20px;
            color: $txt-light;
            font-weight: $bold;
            border: none;
            margin-bottom: 20px;
            cursor: pointer;

            &:hover {
                background-color:$txt-light ;
                color: $primary-color;
            }
        }
    }
}


</style>