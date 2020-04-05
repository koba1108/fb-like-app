<template>
  <aside>
    <div v-for="i in 5" :key="i">
      <a v-for="(m, index) in menus" :key="index" :class="{current: i === 0 && m.current}">
        <i class="material-icons">{{ m.icon }}</i>
        <span>{{ m.text }}</span>
      </a>
      <a v-if="i === 3">
        <i class="material-icons">keyboard_arrow_down</i>
        <span>もっと見る</span>
      </a>
    </div>
  </aside>
</template>

<script>
  const menus = [
    {
      current: true,
      icon: 'home',
      text: 'ホーム',
    },
    {
      current: false,
      icon: 'trending_up',
      text: '急上昇',
    },
    {
      current: false,
      icon: 'folder_special',
      text: '登録チャンネル',
    },
    {
      current: false,
      icon: 'ondemand_video',
      text: 'Originals',
    },
  ]
  export default {
    name: 'Sidebar',
    computed: {
      menus: () => menus,
    },
  }
</script>

<style lang="scss" scoped>
  aside {
    div {
      padding: 12px 0;
      border-bottom: solid 1px lightgray;

      a {
        color: dimgray;
        height: 40px;
        display: flex;
        align-items: center;

        &.current {
          color: #FF0000;
        }

        &:hover {
          background-color: lightgray;
        }

        i {
          margin: 0 24px;
        }

        span {
          color: #000000;
          font-size: 1.4rem;
        }
      }
    }
  }
</style>
