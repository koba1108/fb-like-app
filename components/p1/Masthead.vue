<template>
  <header>
    <div class="menu">
      <button class="material-icons">menu</button>
    </div>
    <a>
      <img class="logo" src="/img/youtube.png">
    </a>
    <form action="#" class="search-box" @click="doSearch">
      <div class="container">
        <div class="input-wrapper">
          <label>
            <input type="text" placeholder="検索" v-model="searchWord">
          </label>
        </div>
      </div>
      <button class="material-icons">search</button>
    </form>
    <div class="btn-area">
      <button class="material-icons">video_call</button>
      <button class="material-icons">apps</button>
      <button class="material-icons">notifications</button>
      <Avatar :size="40"/>
    </div>
  </header>
</template>

<script>
  import Avatar from '../Avatar'

  export default {
    name: 'Masthead',
    components: { Avatar },
    data() {
      return {
        searchWord: '',
      }
    },
    methods: {
      doSearch() {
        console.log('doSearch', this.searchWord)
      },
    },
  }
</script>

<style lang="scss" scoped>
  header {
    display: flex;
    justify-items: start;
    align-items: center;

    button {
      color: dimgray;
      height: 40px;
      width: 40px;
      background-color: #ffffff;
      border: solid 0;
      border-radius: 50%;

      &:focus {
        outline: none;
      }

      &:active {
        background-color: lightgray;
      }
    }

    .menu {
      margin: 16px;
    }

    .logo {
      margin-left: 8px;
      height: auto;
      width: 100px;
      margin-right: 16px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .search-box {
      height: 30px;
      width: 320px;
      display: flex;
      justify-content: center;
      align-items: center;

      @media screen and (max-width: 660px) {
        display: none;
      }

      .container {
        width: 100%;
        max-width: 400px;
        height: 100%;
        padding: 2px 6px;
        border: solid 1px lightgray;
        border-radius: 2px 0 0 2px;
        border-right: none;
        display: flex;
        justify-content: left;
        align-items: center;

        .input-wrapper {
          width: 100%;
          height: 100%;
          display: flex;
          justify-content: left;
          align-items: center;

          input[type=text] {
            border: none;
            height: 100%;
            width: 100%;
            line-height: 24px;
            font-size: 1.6rem;

            &:focus {
              outline: none;
            }
          }
        }
      }

      button {
        height: 36px;
        width: 80px;
        padding: 2px 6px;
        background-color: #E1E1E1;
        border: solid 1px lightgray;
        border-radius: 0 2px 2px 0;

        &:active {
          background-color: darkgray;
        }
      }
    }

    .btn-area {
      margin-left: auto;
      margin-right: 16px;
      display: flex;
      justify-content: left;
      align-items: center;

      button {
        margin-right: 16px;
      }
    }
  }
</style>
