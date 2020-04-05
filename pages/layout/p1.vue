<template>
  <div class="card-box">
    <template v-for="c in 4">
      <div class="title">あなたへのおすすめ</div>
      <div class="card-container">
        <div v-for="i in 8" :key="i" class="card">
          <img class="thumbnail" src="http://via.placeholder.com/480x270">
          <div class="v-box">
            <div class="v-title">
              <span>タイトル</span>
              <button class="menu-btn material-icons">more_vert</button>
            </div>
            <div class="v-desc">しょうさい</div>
          </div>
        </div>
      </div>
      <div class="underline">
        <span/>
      </div>
    </template>
  </div>
</template>

<script>
  export default {
    name: 'p1',
    layout: 'p1',
  }
</script>

<style lang="scss" scoped>
  .card-box {
    display: flex;
    flex-direction: column;
    padding: 24px;

    .title {
      margin: 12px 8px;
      font-size: 2rem;
    }

    .card-container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr 1fr;

      @media screen and (min-width: 660px) {
        grid-template-columns: 1fr 1fr 1fr;
      }

      @media screen and (min-width: 1313px) {
        grid-template-columns: 1fr 1fr 1fr 1fr;
      }

      .card {
        padding: 8px;

        .thumbnail {
          height: 100%;
          width: 100%;
        }

        .v-box {
          .v-title {
            width: 100%;
            display: flex;
            flex-direction: row;
            justify-content: flex-start;

            button {
              display: none;
              color: gray;
              background-color: transparent;
              margin-left: auto;
              border: solid 0;

              &:hover {
                color: darkslategray;
              }

              &:focus {
                outline: none;
              }
            }

            &:hover {
              button {
                display: block;
              }
            }
          }

          .v-desc {
            font-size: 1.4rem;
            color: dimgray;
          }
        }
      }
    }

    .underline {
      text-align: center;

      span {
        width: 97%;
        display: inline-block;
        border-bottom: solid 4px lightgray;
      }
    }
  }
</style>
