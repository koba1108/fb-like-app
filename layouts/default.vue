<template>
  <nuxt/>
</template>

<script>
  export default {
    head: {
      bodyAttrs: {
        class: 'fb-app'
      }
    }
  }
</script>

<style lang="scss">
  .fb-app {
    margin: 0;
    padding: 0;
    @media screen and (max-width: 399px) {
      width: 100%;
    }
    @media screen and (min-width: 400px) {
      margin: 0 auto;
      width: 400px;
    }
  }
</style>
