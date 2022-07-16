<template>
  
  <footer>
    <FooterUpperComponent/>
    <FooterMiddleComponent/>
    <FooterBottomComponent/>
  </footer>


</template>

<script>
import FooterUpperComponent from './FooterUpperComponent.vue';
import FooterMiddleComponent from './FooterMiddleComponent.vue'; 
import FooterBottomComponent from './FooterBottomComponent.vue'; 

export default {
  name: 'Footer',
  components:{
    FooterUpperComponent,
    FooterMiddleComponent,
    FooterBottomComponent,
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";

</style>