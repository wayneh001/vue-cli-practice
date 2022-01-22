<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view />
  <button type="button" class="btn btn-success mt-5">{{ name }}</button>

  <!-- App.vue 下的 template 可以視為共通架構，因為在 SPA 的設計思維下，nav 與 footer 是不會被替換的，頁面的跳動只改變 router-view，因此放置在此頁面的所有 html 標籤，都會在各個 views 分頁中呈現，如 button -->
</template>

<script>
export default {
  data () {
    return {
      name: process.env.VUE_APP_NAME // process 為固定用法
    }
  }
}
</script>
<style lang="scss">
@import "bootstrap";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
