<template>
  <div>
    <Vue2InteractDraggable
      v-for="(c, index) in cards"
      :key="index"
      class="card-container"
      :interact-out-of-sight-x-coordinate="500"
      :interact-max-rotation="15"
      :interact-x-threshold="200"
      :interact-y-threshold="200"
      @draggedUp="swipeT(c)"
      @draggedDown="swipeB(c)"
      @draggedLeft="swipeL(c)"
      @draggedRight="swipeR(c)"
    >
      <img
        class="card"
        :class="{ top: index === 0 }"
        :src="c.url"
        alt="card"
      />
    </Vue2InteractDraggable>
  </div>
</template>

<script>
  const imgUrl = 'http://via.placeholder.com/500x700'
  export default {
    name: 'p2',
    layout: 'p2',
    data() {
      return {
        cards: [
          { id: 1, url: imgUrl },
          { id: 2, url: imgUrl },
          { id: 3, url: imgUrl },
          { id: 4, url: imgUrl },
          { id: 5, url: imgUrl },
        ],
      }
    },
    methods: {
      swipeT({ id }) {
        this.cards = this.cards.filter(c => c.id !== id)
      },
      swipeB({ id }) {
        this.cards = this.cards.filter(c => c.id !== id)
      },
      swipeL({ id }) {
        this.cards = this.cards.filter(c => c.id !== id)
      },
      swipeR({ id }) {
        this.cards = this.cards.filter(c => c.id !== id)
      },
    },
  }
</script>

<style lang="scss" scoped>
  .card-container {
    position: fixed;
    display: flex;
    justify-content: center;
    align-items: center;

    .card {
      height: 90%;
      width: 90%;
      margin: 8px;
      border-radius: 10px;

      &.top {
        pointer-events: auto !important;
      }
    }
  }
</style>
