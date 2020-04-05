<template>
  <div id="app">
    <Masthead id="masthead"/>
    <nav id="navigation">なび</nav>
    <div id="sidebar">メニュー</div>
    <nuxt id="content"/>
  </div>
</template>

<script>
  import Masthead from '../components/p1/Masthead'

  export default {
    components: { Masthead },
    head: {
      bodyAttrs: {
        class: 'p1-app',
      },
    },
  }
</script>

<style lang="scss">
  html {
    font-size: 62.5%;

    a, button {
      cursor: pointer;
    }

    button {
      padding: unset;
    }

    .p1-app {
      margin: unset;
      font-size: 1.6rem;

      #app {
        height: 100vh;
        width: 100vw;
        display: grid;
        grid-template-columns: 72px 1fr; // 横
        grid-template-rows: 56px 1fr; // 縦

        #masthead {
          grid-column: 1/3;
        }

        #navigation {
          background-color: orangered;
          @media screen and (max-width: 500px) {
            display: none;
          }
        }

        #content {
          background-color: green;
          @media screen and (max-width: 500px) {
            grid-column: 1/3;
          }
        }

        #sidebar {
          background-color: bisque;
          display: none;
        }
      }
    }
  }
</style>
