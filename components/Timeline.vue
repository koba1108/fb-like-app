<template>
  <section>
    <div v-for="(t, index) in timelines" :key="index" class="article">
      <TheSpacer/>
      <div class="personal">
        <img class="avatar" :src="avatar" alt="avatar">
        <div>
          <span v-if="t.name">{{ t.name }}</span>
          <br/>
          <span v-if="t.publishedAt">{{ t.publishedAt }}・<i class="material-icons">people</i></span>
        </div>
      </div>
      <div>
        <span class="desc">{{ t.text }}</span>
        <div v-for="image in t.images" :key="image" class="image-area">
          <img :src="image" alt="main">
        </div>
      </div>

      <div class="btn-area">
        <a>
          <span class="material-icons">thumb_up</span>
          <span class="text">いいね！</span>
        </a>
        <a>
          <span class="material-icons">message</span>
          <span class="text">コメントする</span>
        </a>
        <a>
          <span class="material-icons">share</span>
          <span class="text">シェア</span>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
  import TheSpacer from './TheSpacer'

  const timeline = {
    name: '小林 良昇',
    publishedAt: '3時間前',
    text: 'こここっここここここｋ',
    images: [
      'http://via.placeholder.com/400x300',
    ],
  }
  export default {
    name: 'Timeline',
    components: {
      TheSpacer,
    },
    props: {
      avatar: {
        type: String,
        default: '/img/avatar.jpg',
      },
      timelines: {
        type: Array,
        default: () => [
          timeline, timeline, timeline,
        ],
      },
    },
  }
</script>

<style lang="scss" scoped>
  .article {
    .personal {
      display: flex;
      justify-items: start;
      align-items: center;
      padding: 4px;

      .avatar {
        height: 48px;
        width: 48px;
        border-radius: 50%;
      }

      vertical-align: middle;

      span {
        margin-left: 8px;
      }
    }

    .image-area {
      display: grid;

      img {
        max-width: 100vw;
      }
    }

    .desc {
      white-space: pre;
    }

    .btn-area {
      font-size: small;
      border-top: solid 1px lightgray;
      height: 32px;
      display: flex;
      justify-content: center;
      align-items: center;

      a {
        height: 70%;
        width: 33%;
        display: flex;
        justify-content: center;
        align-items: center;

        span {
          vertical-align: middle;

          &.text {
            margin-left: 8px;
            font-weight: bold;
          }
        }

        @media screen and (max-width: 320px) {
          font-size: 12px;
        }
      }
    }
  }
</style>
