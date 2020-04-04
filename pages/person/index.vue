<template>
  <div>
    <TheHeader title="小林良昇"/>
    <div>
      こんてんつ２
    </div>
    <TheNav/>
  </div>
</template>

<script>
  import TheNav from '../../components/TheNav'
  import TheHeader from '../../components/TheHeader'

  export default {
    name: 'index',
    components: { TheHeader, TheNav },
  }
</script>

<style scoped>

</style>
