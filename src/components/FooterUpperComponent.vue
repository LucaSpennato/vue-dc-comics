<template>
  <section class="foot-upper-section">
    <div class="container">
        <div class="row py-5 justify-content-center">

            <div class="col-6 py-3 col-md-2 py-md-0"
                    v-for="(link, index) in userShopSuggestions"
                :key="index">
                <a :href="link.url" @click.prevent>
                    <img :src="imgsPath(link)" :alt="link.text">
                    </a>
                    <span class="ps-2">{{ link.text }}</span>
            </div>

        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: 'FootUpperSection',
    data(){
        return{
            userShopSuggestions: 
            [
                {
                    text: 'digital comics',
                    url: '#',
                    icon: 'comics-digital-comics.png',
                },
                {
                    text: 'dc merchandise',
                    url: '#',
                    icon: 'comics-merchandise.png',
                },
                {
                    text: 'subscription',
                    url: '#',
                    icon: 'comics-subscriptions.png',
                },
                {
                    text: 'comic shop locator',
                    url: '#',
                    icon: 'comics-shop-locator.png',
                },
                {
                    text: 'dc power visa',
                    url: '#',
                    icon: 'dc-power-visa.svg',
                },
                
            ]
        };
    },
    methods:
    {
        imgsPath: function (array){
           return require('../assets/img/buy-' + array.icon);
        }
    }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";
@import '../styles/variables.scss';

.foot-upper-section{
  background-color: $primaryColor;

    span{
        color: white;
        text-transform: uppercase;
        font-size: .8rem;
    }
    img{
        height: 3rem;
    }
}

</style>