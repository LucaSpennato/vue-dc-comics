<template>
  <footer>
    <div class="container-fluid p-0 bg-footer-img">
      <section class="foot-top-section">
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
                            <a :href="link.url">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="col-6 bg-logo"></div>
          </div>
        </div>
      </section>
    </div>

    <section class="bottom-section">
      <div class="container-fluid p-0 bg-dark">
        <div class="container">
          <div class="row p-4 justify-content-between align-items-center">
            <div class="col-2">
              <a class="btn btn-outline-primary text-light p-2">
                SIGN-UP NOW!
              </a>
            </div>
            <div class="col-4">
                <ul class="d-flex justify-content-center align-items-center">
                    <li><h5 class="m-0">follow us</h5></li>
                    <li 
                    v-for="(iconLink, index) in footerIconLinks"
                    :key="index">
                        <a :href="iconLink.url"
                            target="_blank">
                            <img 
                            :src="iconsPath(iconLink)"
                            :alt="iconLink.icon"/></a>
                    </li>
                </ul>
            </div>
          </div>
        </div>
      </div>
    </section>
  </footer>
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
           
           footerIconLinks: [
            {
                icon: 'facebook',
                url: 'https://www.facebook.com/dc/',
            },
            {
                icon: 'twitter',
                url: 'https://twitter.com/dccomics/',
            },
            {
                icon: 'youtube',
                url: 'https://www.youtube.com/channel/UCiifkYAs_bq1pt_zbNAzYGg',
            },
            {
                icon: 'pinterest',
                url: 'https://www.pinterest.it/dccomics/',
            },
            {
                icon: 'periscope',
                url: 'https://www.google.com/maps/place/Burbank,+California,+Stati+Uniti/@34.1820055,-118.3602306,13z/data=!3m1!4b1!4m5!3m4!1s0x80c295152818c595:0x307791af901f8ad4!8m2!3d34.1808392!4d-118.3089661',
            },
           ],
        };
    },
    methods: {
        iconsPath: function (array){
           return require('../assets/img/footer-' + array.icon + '.png');
        }
    }    
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

  section .bg-logo {
    background-image: url(../assets/img/dc-logo-bg.png);
    background-position: center;
    background-repeat: no-repeat;
  }
  .bottom-section {
    h5 {
      color: $primaryColor;
    }

    a {
    padding: 0 0.5rem;
    }
    
  }
}
</style>