<template>
  <section>
    <div class="tweet-box">
      <img src="/img/avatar.jpg" alt="avatar">
      <span>今なにしてる？</span>
    </div>
    <div class="btn-area">
      <a>
        <span class="material-icons green">video_call</span>
        <span class="text">ライブ動画</span>
      </a>
      <a>
        <span class="material-icons light-green">insert_photo</span>
        <span class="text">写真</span>
      </a>
      <a>
        <span class="material-icons pink">place</span>
        <span class="text">チェックイン</span>
      </a>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'TweetBox',
  }
</script>

<style lang="scss" scoped>
  section {
    padding: 0 4px;
  }

  .tweet-box {
    height: 52px;
    display: flex;
    justify-content: left;
    align-items: center;
    padding-bottom: 4px;

    img {
      height: 48px;
      width: 48px;
      border-radius: 50%;
    }

    span {
      font-weight: bold;
      margin-left: 8px;
    }
  }

  .btn-area {
    border-top: solid 1px lightgray;
    height: 32px;
    display: flex;
    justify-content: center;
    align-items: center;

    > *:first-child {
      border-right: solid 0.5px lightgray;
    }

    > *:last-child {
      border-left: solid 0.5px lightgray;
    }

    a {
      height: 70%;
      width: 33%;
      display: flex;
      justify-content: center;
      align-items: center;

      .green {
        color: green;
      }

      .light-green {
        color: lightgreen;
      }

      .pink {
        color: deeppink;
      }

      span {
        vertical-align: middle;

        &.text {
          font-weight: bold;
          font-size: small;
        }
      }
    }
  }
</style>
