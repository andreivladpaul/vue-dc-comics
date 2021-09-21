<template>
    <div class="footer">
        <div class="footer-top">
            <div class="container">
                <div class="top-left p-tb">
                    <div class="col">
                        <ul class="list-link"><span class="title-list">DC COMICS</span>
                            <li v-for="(link, index) in footDCComics" :key="index"><a href="">{{link.text}}</a></li>
                        </ul>
                        <ul class="list-link"><span class="title-list">SHOP</span>
                            <li v-for="(link, index) in footShop" :key="index"><a href="">{{link.text}}</a></li>
                        </ul>
                    </div>
                    <div class="col">
                        <ul class="list-link"><span class="title-list">DC</span>
                            <li v-for="(link, index) in footDC" :key="index"><a href="">{{link.text}}</a></li>
                        </ul>
                    </div>
                    <div class="col">
                        <ul class="list-link"><span class="title-list">SITES</span>
                            <li v-for="(link, index) in footSites" :key="index"><a href="">{{link.text}}</a></li>
                        </ul>
                    </div>
                    
                </div>
                <div class="top-right">
                    <img src="../assets/img/dc-logo-bg.png" alt="Logo DC">
                </div>
            </div>
        </div>
        <div class="footer-bottom p-tb">
            <div class="container">
                <div class="sign-up">
                    <button> SIGN-UP NOW!</button>
                </div>
                <div class="socials">
                    <span class="follow">FOLLOW US</span>
                    <div v-for="(social, index) in socialsLink" :key="index" class="img-social">
                        <a :href="social.url"><img :src="require(`../assets/${social.icon}`)" :alt="social.name"></a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Links from '@/assets/data/Links.js'
import Socials from '@/assets/data/Socials.js'
export default {
    name: 'Footer',
    data(){
        return{
            footDCComics : Links.footDCComics,
            footShop : Links.footShop,
            footDC : Links.footDC,
            footSites : Links.footSites,
            socialsLink: Socials,
        }
    }
}
</script>

<style scoped lang="scss">
@import '@/style/general';

.p-tb{
    padding: 20px 0px;
}

.list-link{
    color: #c7c7c7; 
    font-size: $fs-xs; 
    list-style: none;
    margin: 15px 0px;
    a {
        text-decoration: none;
        line-height: 20px;
        color: inherit;

        &:hover{
            color: $primary-color;
        }
    }

    .title-list{
        display: block;
        margin-bottom: 15px;
        color: white; 
        font-size: $fs-lg; 
        font-weight: $bold; 
    }
}

.footer-top{
    height: 400px;
    background-image: url('../assets/img/footer-bg.jpg');

    .container{
        display: flex;
        justify-content: space-between;

        .top-left{
            display: flex;
            justify-content: space-between;

            .col {
                margin-right: 25px;
            }
        }

        .top-right{
            width: 600px;

            img{
                object-fit: cover;
                width: 100%;
                height: 100%;
            }
        }
    }
}

.footer-bottom{
    width: 100%; 
    height: 150px; 
    background-color: $dark-color;

    .container{
        @include center(vertical);
        justify-content: space-between;

        button{
            border: 2px solid $primary-color;
            padding: 15px 25px;
            color: $txt-light;
            font-size: $fs-lg;
            cursor: pointer;
            background: linear-gradient(to right, transparent 50%, $primary-color 50%) left;
            background-size: 250%;
            transition: .5s ease-out;

            &:hover{
                background-position: right;
            }
        }

        .follow {
            color: $primary-color;
            font-weight: $bold;
            font-size: $fs-xl;
        }

        .socials{
            @include center(vertical);
            justify-content: space-around;

            .img-social{ 
                width: 40px;
                margin-left: 20px;

                img{
                    width: 100%;
                    
                }

                &:hover{
                    filter: brightness(1.3);
                }
            }
        }
    }
}



</style>