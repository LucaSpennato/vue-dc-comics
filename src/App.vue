<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <Header/>
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

</style>
