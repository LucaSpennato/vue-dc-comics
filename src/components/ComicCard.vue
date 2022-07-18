<template>
  <div class="comic my-5 col-2">
        <img :src="thumb" 
            :alt="type.alt">
        <h6 class="mt-2">
            {{ series }}
        </h6>
    </div>
</template>

<script>
export default {
    name: 'ComicCard',
    props:{
      thumb: String,
      series: String,
      type: {
        alt: String,
        required: true,
      }
    },
}
</script>

<style lang="scss">

.comic{
        height: 10rem;
        h6{
            text-transform: uppercase;
        }
        img{
            object-fit: cover;
            object-position: top;
            width: 100%;
            height: 100%;
        }
    }
</style>