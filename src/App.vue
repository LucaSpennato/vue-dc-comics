<template>
  <div id="app">
    <Header/>
    <MainContent/>
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


</style>
