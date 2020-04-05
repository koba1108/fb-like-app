<template>
  <div id="app">
    <Masthead id="masthead"/>
    <Navigator id="navigation"/>
    <Sidebar id="sidebar"/>
    <nuxt id="content"/>
  </div>
</template>

<script>
  import Masthead from '../components/p1/Masthead'
  import Navigator from '../components/p1/Navigator'
  import Sidebar from '../components/p1/Sidebar'

  export default {
    components: { Sidebar, Navigator, Masthead },
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
        @media screen and (min-width: 1313px) {
          grid-template-columns: 240px 1fr; // 横
        }

        #masthead {
          grid-column: 1/3;
        }

        #navigation {
          @media screen and (max-width: 790px) {
            display: none;
          }
          @media screen and (min-width: 1313px) {
            display: none;
          }
        }

        #content {
          background-color: #F5F5F5;
          @media screen and (max-width: 790px) {
            grid-column: 1/3;
          }
        }

        #sidebar {
          display: none;
          @media screen and (min-width: 1313px) {
            display: block;
          }
        }
      }
    }
  }
</style>
