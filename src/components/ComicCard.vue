<template>
  <div class="comic my-5 col-2">
        <img :src="thumb" 
            :alt="type.alt">
        <h6 class="mt-2">
            {{ series }}
        </h6>
        <div class="price">{{ price }}</div>
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
      },
      price: [String, Number],
    },
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

.comic{
    position: relative;
    height: 10rem;

        &:hover .price{
            display: block;
        }
        h6{
            text-transform: uppercase;
        }
        .price{
            position: absolute;
            top: 50%;
            left: 1rem;
            font-weight: bold;
            color: yellow;
            display: none;
        }
        img{
            object-fit: cover;
            object-position: top;
            width: 100%;
            height: 100%;
        }
    }
</style>