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

      <FooterComponent/>

  </div>

</template>

<script>
import Header from './components/Header.vue';
import MainContent from './components/MainContent.vue'
import FooterComponent from './components/FooterComponent.vue'

export default {
  name: 'App',
  components: {
    Header,
    MainContent,
    FooterComponent,
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";
@import "./styles/variables.scss";

.bg-MainFix{
  background-color: $mainContentBgColor;
}
</style>
