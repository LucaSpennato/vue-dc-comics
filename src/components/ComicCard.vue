<template>
  <div class="comic my-5 col-2">
        <img :src="thumb" 
            alt="">
        <div class="mt-2 fs-6">
            {{ series }}
    </div>
    </div>
</template>

<script>
export default {
    name: 'ComicCard',
    props:{
      thumb: String,
      series: String,
    },
}
</script>

<style lang="scss">

.comic{
        height: 10rem;
        img{
            object-fit: cover;
            object-position: top;
            width: 100%;
            height: 100%;
        }
    }
</style>