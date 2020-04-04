<template>
  <section>
    <nav>
      <div class="material-icons" :class="{ current: isHome }" @click="$router.push('/')">home</div>
      <div class="material-icons" :class="{ current: isPerson }" @click="$router.push('/person')">person_outline</div>
      <div class="material-icons" :class="{ current: isPeople }">people_outline</div>
      <div class="material-icons" :class="{ current: isFlag }">flag</div>
      <div class="material-icons" :class="{ current: isNotification }">notifications</div>
      <div class="material-icons" :class="{ current: isMenu }">menu</div>
    </nav>
  </section>
</template>

<script>
  export default {
    name: 'TheNav',
    computed: {
      isHome() {
        return this.$route.path === '/'
      },
      isPerson() {
        return this.$route.path === '/person'
      },
      isPeople() {
        return this.$route.path === 'home' // todo:
      },
      isFlag() {
        return this.$route.path === 'home' // todo:
      },
      isNotification() {
        return this.$route.path === 'home' // todo:
      },
      isMenu() {
        return this.$route.path === 'home' // todo:
      },
    },
  }
</script>

<style lang="scss" scoped>
  section {
    height: 52px;
    position: fixed;
    bottom: 0;
    @media screen and (max-width: 399px) {
      width: 100%;
    }
    @media screen and (min-width: 400px) {
      margin: 0 auto;
      width: 400px;
    }

    nav {
      z-index: 1000;
      background-color: white;
      position: absolute;
      bottom: 0;
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;

      div {
        text-align: center;
        height: 100%;
        width: 16%;
        display: flex;
        justify-content: center;
        align-items: center;

        &.current {
          color: #3b5998;
          border-top: solid 2px #3b5998;
        }
      }
    }
  }
</style>
