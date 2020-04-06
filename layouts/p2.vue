<template>
  <div id="app">
    <Masthead2 id="header"/>
    <nuxt id="content"/>
    <ActionBtnContainer id="footer"/>
  </div>
</template>

<script>
  import Masthead2 from '../components/p2/Masthead'
  import ActionBtnContainer from '../components/p2/ActionBtnContainer'

  export default {
    name: 'p2',
    components: { ActionBtnContainer, Masthead2 },
    head: {
      bodyAttrs: {
        class: 'tinder-app',
      },
    },
  }
</script>

<style lang="scss">
  html, body, #__nuxt, #__layout, #app {
    height: 100%;
  }

  button {
    &:focus {
      outline: none;
    }
  }

  // body class
  .tinder-app {
    margin: 0;
    padding: 0;
    font-size: 1.6rem;
    background-color: #F5F5F5;

    #app {
      display: flex;
      flex-direction: column;

      #header {
        min-height: 52px;
      }

      #content {
        height: 100%;
      }

      #footer {
        min-height: 84px;
      }
    }
  }
</style>
