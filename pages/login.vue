<template>
  <div>
    <div>
      <h1>なんかロゴ</h1>
      <div>説明テキストたち</div>
    </div>
    <div>
      <h3>ログイン</h3>
      <div>
        <button @click="loginWithRedirect">loginWithRedirect</button>
        <button @click="loginWithPopup">loginWithPopup</button>
        <button>Facebook</button>
        <button>Twitter</button>
        <button>Line</button>
      </div>
      <form>
        <h3>登録済みのメールアドレスでログイン</h3>
        <form action="#">
          <label>
            <input type="email">
          </label>
          <label>
            <input type="password">
          </label>
          <button>メールアドレスでログイン</button>
        </form>
      </form>
      <button @click="logout">Logout</button>
    </div>
  </div>
</template>

<script>
  import createAuth0Client from '@auth0/auth0-spa-js'

  const AUTH0_DOMAIN = 'ykoba.auth0.com'
  const AUTH0_CLIENT_ID = 'ZTCcIZpJivGk5r4w5BQs6s94ttQO4day'
  const AUTH0_CALLBACK_URL = 'http://localhost:3000/callback'

  export default {
    name: 'login',
    data() {
      return {
        auth0: null,
      }
    },
    methods: {
      loginWithRedirect() {
        this.auth0.loginWithRedirect()
      },
      loginWithPopup() {
        this.auth0.loginWithPopup()
      },
      logout() {
        this.auth0.logout()
      }
    },
    async created() {
      this.auth0 = await createAuth0Client({
        domain: AUTH0_DOMAIN,
        client_id: AUTH0_CLIENT_ID,
        redirect_uri: AUTH0_CALLBACK_URL,
      })
    }
  }
</script>

<style scoped>

</style>
