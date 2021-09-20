<template>
    <main>
        <div class="products layout">
            <p>-->Content Go Here-->  </p>
        </div>
    </main>
    
    
</template>

<script>
 export default {
     name: 'Main'
 }
</script>

<style scoped lang="scss">
@import '../style/vars';

main {
    background-color: $grey;
}
.products {
    padding: 40px;
    p {
        color: #fff;
        font-size: 50px;
    }
}

</style>