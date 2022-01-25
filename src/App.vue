<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light mb-5">
    <div class="container">
      <a class="navbar-brand" href="#">Navbar</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/about">About</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" :to="{ name: 'NewPage' }"
              >NewPage</router-link
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <div class="container">
    <router-view />
    <button type="button" class="btn btn-success mt-5">{{ name }}</button>
  </div>

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

// #nav {
//   padding: 30px;

//   a {
//     font-weight: bold;
//     color: #2c3e50;

//     &.router-link-exact-active {
//       color: #42b983;
//     }
//   }
// }
</style>
