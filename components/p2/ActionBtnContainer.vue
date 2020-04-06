<template>
  <div class="container">
    <button class="small orange fas fa-undo-alt"/>
    <button class="fas red fa-times"/>
    <button class="small blue fas fa-star"/>
    <button class="pink fas fa-heart"/>
    <button class="small deep-blue fas fa-cog"/>
  </div>
</template>

<script>
  export default {
    name: 'ActionBtnContainer',
  }
</script>

<style lang="scss" scoped>
  .container {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;

    button {
      margin: auto;
      background-color: #ffffff;
      color: gray;
      height: 52px;
      width: 52px;
      border: unset;
      border-radius: 50%;
      font-size: 125%;

      &:active {
        transform: scale(0.8, 0.8);
        transition: all 0.5s ease;
      }

      &.small {
        height: 44px;
        width: 44px;
      }

      &.orange {
        color: orangered;
      }

      &.red {
        color: red;
      }

      &.blue {
        color: cornflowerblue;
      }

      &.pink {
        color: deeppink;
      }

      &.deep-blue {
        color: deepskyblue;
      }
    }
  }
</style>
