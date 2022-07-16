<template>
  <footer>
    <div class="container-fluid p-0 bg-footer-img">
      <section class="foot-top-section">
        <div class="container">
          <div class="row">
            <div class="row col-6 col-6 p-4">

                <div class="col-4 p-0 d-inline"
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
          <div class="row p-4 justify-content-between">
            <div class="col-2">
              <button class="btn btn-outline-primary text-light">
                SIGN-UP NOW!
              </button>
            </div>
            <div class="col-4">
              <h5>follow us</h5>
              <div class="icon-wrapper">
                <a href="#"
                  ><img src="../assets/img/footer-facebook.png" alt=""
                /></a>
                <a href="#"
                  ><img src="../assets/img/footer-twitter.png" alt=""
                /></a>
                <a href="#"
                  ><img src="../assets/img/footer-youtube.png" alt=""
                /></a>
                <a href="#"
                  ><img src="../assets/img/footer-pinterest.png" alt=""
                /></a>
                <a href="#"
                  ><img src="../assets/img/footer-periscope.png" alt=""
                /></a>
              </div>
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
                            text: 'MAD Magazine',
                            url: '#',
                        },
                        {
                            text: 'Dc Kids',
                            url: '#',
                        },
                        {
                            text: 'DC Universe',
                            url: '#',
                        },
                        {
                            text: 'DC Power Visa',
                            url: '#',
                        },
                    ],
                },
                {
                    linksGroup: 'dc',
                    links: [
                        {
                            text: 'Terms Of Use',
                            url: '#',
                        },
                        {
                            text: 'Privacy policy (new)',
                            url: '#',
                        },
                        {
                            text: 'Ad Choices',
                            url: '#',
                        },
                        {
                            text: 'Advertising',
                            url: '#',
                        },
                        {
                            text: 'Jobs',
                            url: '#',
                        },
                        {
                            text: 'Subscriptions',
                            url: '#',
                        },
                        {
                            text: 'Talent Workshops',
                            url: '#',
                        },
                        {
                            text: 'CPSC Certificates',
                            url: '#',
                        },
                        {
                            text: 'Ratings',
                            url: '#',
                        },
                        {
                            text: 'Shop Help',
                            url: '#',
                        },
                        {
                            text: 'Conctact Us',
                            url: '#',
                        },
                        
                    ],
                },
                {    
                    linksGroup: 'shop',
                    links: [
                        {
                            text: 'Shop DC',
                            url: '#',
                        },
                        {
                            text: 'Shop DC Collectibles',
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
    list-style: none;
  }
  li {
    line-height: 100%;
  }
  li a {
    text-decoration: none;
    color: gray;
    font-size: 0.7rem;

    &:hover {
      color: $primaryTextColor;
    }
  }

  section .bg-logo {
    background-image: url(../assets/img/dc-logo-bg.png);
    background-position: center;
    background-repeat: no-repeat;
  }
  .bottom-section {
    h5 {
      color: $primaryTextColor;
      display: inline-block;
      margin-right: 0.3rem;
    }

    .icon-wrapper {
      display: inline-block;

      a {
        padding: 0 0.5rem;
      }
    }
  }
}
</style>