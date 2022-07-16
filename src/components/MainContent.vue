<template>
  <main>
    <div class="container">
      <div class="p-5">
          --> Content goes here
      </div>
    </div>
  </main>
</template>

<script>
export default {
    name:'MainContent',
}
</script>

<style lang="scss">
@import '../styles/variables.scss';
    main{
        color: white;
        font-weight: bold;
        font-size: 1.5rem;
        background-color: $mainContentBgColor;
    }
</style>