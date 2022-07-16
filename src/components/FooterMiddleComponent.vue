<template>
      <section class="foot-top-section p-0 bg-footer-img">

        <div class="container">

          <div class="row">

            <div class="row col-6 p-5">

                <div class="col-4 d-inline"
                v-for="(list, index) in footerNavLinks"
                :key="index">

                    <ul>
                        <h5>{{ list.linksGroup }}</h5>

                        <li v-for="(link, index) in footerNavLinks[index].links"
                        :key="index">
                            <a :href="link.url"
                            @click.prevent>{{ link.text }}</a>
                        </li>

                    </ul>

                </div>

            </div>

            <!-- logo on right -->
            <div class="col-6 bg-logo"></div>
            </div>

        </div>
      </section>
</template>

<script>
export default {
  name: "FooterContent",
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
  h5 {
    color: white;
    text-transform: uppercase;
  }
  ul {
    padding: 0;
    margin: 0;
    list-style: none;
  }
  li {
    line-height: 100%;
  }
  .foot-top-section li a {
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