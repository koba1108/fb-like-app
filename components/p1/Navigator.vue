<template>
  <nav>
    <a class="current">
      <i class="material-icons">home</i>
      <span>ホーム</span>
    </a>
    <a>
      <i class="material-icons">trending_up</i>
      <span>急上昇</span>
    </a>
    <a>
      <i class="material-icons">folder_special</i>
      <span>登録チャンネル</span>
    </a>
    <a>
      <i class="material-icons">ondemand_video</i>
      <span>Originals</span>
    </a>
    <a>
      <i class="material-icons">video_library</i>
      <span>ライブラリ</span>
    </a>
  </nav>
</template>

<script>
  export default {
    name: 'Navigator',
  }
</script>

<style lang="scss" scoped>
  nav {
    display: flex;
    flex-direction: column;
    justify-items: center;
    align-items: center;

    a {
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 74px;

      span {
        font-size: 1rem;
      }

      &.current {
        i, span {
          color: #FF0000;
        }
      }

      &:active {
        background-color: lightgray;
      }

      &:hover {
        background-color: lightgray;
      }

      i {
        padding: 6px;
        color: dimgray;
        border: solid 0;

        &:focus {
          outline: none;
        }
      }
    }
  }

</style>
