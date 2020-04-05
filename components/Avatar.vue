<template>
  <a :style="style" >
    <img src="/img/avatar.jpg" :style="style" alt="avatar">
  </a>
</template>

<script>
  export default {
    name: 'Avatar',
    props: {
      size: {
        type: Number,
        default: 40,
      },
    },
    computed: {
      style() {
        return {
          height: this.size + 'px',
          width: this.size + 'px',
          'border-radius': '50%',
        }
      },
    },
  }
</script>

<style lang="scss" scoped>
  a {
    &:active {
      border: solid 2px red;
    }
  }
</style>
