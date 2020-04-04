<template>
  <header>
    <div class="logo">
      <h1>{{ title }}</h1>
    </div>
    <div class="btn-area">
      <button class="material-icons" @click="goSearch">search</button>
      <button class="material-icons" @click="goMessage">textsms</button>
    </div>
  </header>
</template>

<script>
  export default {
    name: 'TheHeader',
    props: {
      title: {
        type: String,
        default: 'facebook',
      }
    },
    methods: {
      goSearch() {
        console.log('goSearch')
      },
      goMessage() {
        console.log('goMessage')
      },
    },
  }
</script>

<style lang="scss" scoped>
  header {
    padding: 8px;
    display: flex;
    height: 52px;
    width: auto;
    justify-content: center;
    align-items: center;

    .logo {
      width: 50%;
      height: 100%;

      h1 {
        margin: 0;
        color: #3b5998;
      }
    }

    .btn-area {
      display: flex;
      justify-content: flex-end;
      align-items: center;
      width: 50%;
      height: 100%;

      button {
        background-color: lightgray;
        height: 40px;
        width: 40px;
        margin-left: 8px;
        border: 0;
        border-radius: 50%;
      }
    }
  }
</style>
