<template>

   <header class="layout">
       <div class="logo">
           <img src="@/assets/dc-logo.png" alt="">
       </div>
       

       <ul>
           <li v-for="(link, index) in links" :key="index" class="upper-case" :class="(link.current==true)? 'active' : null">
               <a :href="link.url">{{link.text}}</a>
           </li>
       </ul>
   </header>
    
</template>

<script >
 export default {
     name: 'Header',
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

<style scoped lang='scss'>

@import '../style/vars';
@import '../style/generals';
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap');

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    
    
    ul {
        display: flex;
        list-style: none;
        justify-content: center;
        align-items: center;

        li{
            &.active {
                padding: 40px 0 35px 0;
                border-bottom: 5px solid $blue;
                
                
                a {
                    color: $blue;
                }
            }
            &:hover {
                padding: 40px 0 35px 0;
                border-bottom: 5px solid $blue;

                a {
                    color: $blue;
                }
            }
        }
   
        li a {
            color: $grey;
            text-decoration: none;
            display: flex;
            font-weight: bold;
            padding: 40px 0;
                   
        
        }
        li:not(:last-child) {
            margin-right: 10px;
        }

        
    }
    .logo {
        width: 100px;
        height: 100px;
    }
    img {
        width: 100%;
        height: 100%;
    }
    
}



</style>
