<template>
  <div class="card">
      <div class="img-card">
          <img :src="prod.thumb" alt="">
      </div>
      <div class="title-card">
          <span>{{prod.series.toUpperCase()}}</span>
      </div>
  </div>
</template>

<script>
export default {
    name: 'ProductCard',
    props: ['prod']
}
</script>


<style lang="scss" scoped>
@import '@/style/general.scss';

    .card{
        float: left;
        margin: 15px;

        .img-card{
            width: 186px ;
            height: 186px;
            cursor: pointer;

            img{
                width: 100%;
                height: 100%;
                object-fit: cover;
                object-position: top;
            }

            &:hover{
                filter: brightness(1.1);
            }
        }

        .title-card{
            max-width: 186px;
            color: $txt-light;
            margin-top: 15px;
            font-size: 12px;
        }
    }

</style>