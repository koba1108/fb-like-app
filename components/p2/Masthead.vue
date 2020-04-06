<template>
  <header>
    <button class="fas fa-user-alt"/>
    <div class="switcher-container">
      <button class="fas fa-fire-alt" :class="{ current: currentTab === 'card' }" @click="currentTab = 'card'"/>
      <button class="fas fa-star" :class="{ current: currentTab === 'like' }" @click="currentTab = 'like'"/>
    </div>
    <button class="fas fa-comments"/>
  </header>
</template>

<script>
  export default {
    name: 'Masthead2',
    data() {
      return {
        currentTab: 'card',
      }
    },
  }
</script>

<style lang="scss" scoped>
  header {
    display: flex;
    flex-direction: row;
    justify-content: center;
    justify-items: center;
    align-items: center;

    button {
      background-color: #F5F5F5;
      color: gray;
      height: 48px;
      width: 48px;
      border: unset;
      border-radius: 50%;
      font-size: 125%;

      &:active {
        transform: scale(0.8, 0.8);
        transition: all 0.5s ease;
      }
    }

    .switcher-container {
      background-color: lightgray;
      margin: auto;
      height: 36px;
      width: 92px;
      border-radius: 20px;
      display: flex;
      flex-direction: row;
      justify-content: flex-start;
      align-items: center;

      :last-child {
        margin-left: auto;
      }

      button {
        height: 36px;
        width: 58px;
        border-radius: 20px;
        background-color: transparent;
        transition: all 0.3s ease;

        &.current {
          color: orange;
          background-color: #ffffff;
          box-shadow: 0 0 1px gray;
        }
      }
    }
  }
</style>
