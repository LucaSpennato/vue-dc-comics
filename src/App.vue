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

    <section class="upper-section">
      <div class="container p-3">
        <FooterUpperComponent/>
      </div>
    </section>

      <Footer/>

  </div>

</template>

<script>
import Header from './components/Header.vue';
import MainContent from './components/MainContent.vue'
import FooterUpperComponent from './components/FooterUpperComponent.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    MainContent,
    FooterUpperComponent,
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
.upper-section{
  background-color: $primaryColor;
}
</style>
