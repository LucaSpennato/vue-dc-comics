<template>
  <section class="bottom-section p-0 bg-dark">
      <div class="container">

        <div class="row p-4 justify-content-between align-items-center">

          <div class="col-2">
            <a class="btn btn-outline-primary text-light p-2"> SIGN-UP NOW! </a>
          </div>

          <div class="col-4">

            <ul class="d-flex justify-content-center align-items-center">

              <li><h5 class="m-0 me-2">follow us</h5></li>

              <li v-for="(iconLink, index) in footerIconLinks" :key="index">
                <a :href="iconLink.url" target="_blank">
                  <img :src="iconsPath(iconLink)" :alt="iconLink.icon"
                /></a>
              </li>

            </ul>

          </div>

        </div>

      </div>

  </section>
</template>

<script>
export default {
  name: "FootDownSection",
  data(){
        return{
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
@import "~bootstrap/scss/bootstrap.scss";
@import "../styles/variables.scss";

.bottom-section{
    h5{
      color: $primaryColor;
      font-weight: bold;
    }
    ul {
    padding: 0;
    margin: 0;
    list-style: none;
    color: $primaryColor;
    } 
    a {
    padding: 0 0.5rem;
    }
}

</style>