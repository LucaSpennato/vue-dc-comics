<template>
      <section class="foot-middle-section p-0 bg-footer-img">

        <div class="container">

          <div class="row">

            <nav class="row col-12 col-lg-6 p-5">

                <div class="col-4 d-inline"
                v-for="(list, index) in footerNavLinks"
                :key="index">

                <FooterNavLinks 
                :listName="list.linksGroup"
                :links="list.links"
                />
                    <!-- <h5>{{ list.linksGroup }}</h5>
                    <ul>

                        <li v-for="(link, liElementIndex) in list.links"
                        :key="liElementIndex">
                            <a :href="link.url"
                            @click.prevent>{{ link.text }}</a>
                        </li>

                    </ul> -->

                </div>

            </nav>

            <!-- logo on right -->
            <div class="col-lg-6 d-none d-lg-block bg-logo"></div>
            </div>

        </div>
      </section>
</template>

<script>
import FooterNavLinks from './FooterNavLinks.vue';
export default {
  name: "FooterContent",
  components:{
    FooterNavLinks,
  },
  data(){
        return{
           footerNavLinks: [
                {
                    linksGroup: 'dc comics',
                    links: [
                        {
                            text: 'characters',
                            url: '#',
                        },
                        {
                            text: 'comics',
                            url: '#',
                        },
                        {
                            text: 'movies',
                            url: '#',
                        },
                        {
                            text: 'tv',
                            url: '#',
                        },
                        {
                            text: 'games',
                            url: '#',
                        },
                        {
                            text: 'collectibles',
                            url: '#',
                        },
                        {
                            text: 'videos',
                            url: '#',
                        },
                        {
                            text: 'fans',
                            url: '#',
                        },
                        {
                            text: 'news',
                            url: '#',
                        },
                        {
                            text: 'shop',
                            url: '#',
                        },
                    ],
                },
                {
                    linksGroup: 'dc',
                    links: [
                        {
                            text: 'terms of use',
                            url: '#',
                        },
                        {
                            text: 'privacy policy (new)',
                            url: '#',
                        },
                        {
                            text: 'ad choices',
                            url: '#',
                        },
                        {
                            text: 'advertising',
                            url: '#',
                        },
                        {
                            text: 'jobs',
                            url: '#',
                        },
                        {
                            text: 'subscriptions',
                            url: '#',
                        },
                        {
                            text: 'talent workshops',
                            url: '#',
                        },
                        {
                            text: 'CPSC certificates',
                            url: '#',
                        },
                        {
                            text: 'ratings',
                            url: '#',
                        },
                        {
                            text: 'shop help',
                            url: '#',
                        },
                        {
                            text: 'conctact us',
                            url: '#',
                        },
                        
                    ],
                },
                {
                    linksGroup: 'sites',
                    links: [
                        {
                            text: 'DC',
                            url: '#',
                        },
                        {
                            text: 'MAD magazine',
                            url: '#',
                        },
                        {
                            text: 'Dc kids',
                            url: '#',
                        },
                        {
                            text: 'DC universe',
                            url: '#',
                        },
                        {
                            text: 'DC power visa',
                            url: '#',
                        },
                    ],
                },
                {    
                    linksGroup: 'shop',
                    links: [
                        {
                            text: 'shop DC',
                            url: '#',
                        },
                        {
                            text: 'shop DC collectibles',
                            url: '#',
                        },
                    ],
                },
                
           ],
  
        };
    },
};
</script>

<style lang="scss">
@import "../styles/variables.scss";

.bg-footer-img {
background-image: url(../assets/img/footer-bg.jpg);
background-repeat: no-repeat;
background-size: cover;
}
footer {
    .foot-middle-section li a {
        text-decoration: none;
        color: gray;
        font-size: 0.7rem;
        text-transform: capitalize;

        &:hover {
        color: $primaryColor;
        }
    }
    .bg-logo {
        background-image: url(../assets/img/dc-logo-bg.png);
        background-position: center;
        background-repeat: no-repeat;
    }
}
</style>