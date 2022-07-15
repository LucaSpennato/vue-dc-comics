<template>
  <div id="app">

    <div class="container-fluid">
      <div class="container p-3">
          <Header/>
      </div>
    </div>

    <div class="container-fluid bg-MainFix">
      <div class="container p-3">
          <MainContent/>
      </div>
    </div>

    <div class="container-fluid bg-footer-img">
      <div class="container">
        <Footer/>
      </div>
    </div>

  </div>

</template>

<script>
import Header from './components/Header.vue';
import MainContent from './components/MainContent.vue'
import Footer from './components/Footer.vue'
export default {
  name: 'App',
  components: {
    Header,
    MainContent,
    Footer,
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";
@import "./styles/variables.scss";

.bg-MainFix{
  background-color: $mainContentBgColor;
}

.bg-footer-img{
  background-image: url(./assets/img/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
}

</style>
