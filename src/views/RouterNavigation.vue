<template>
  <div class="btn-group" role="group" aria-label="Basic example">
    <button type="button" class="btn btn-success" @click="getRoute">
      GET ROUTE
    </button>
    <button type="button" class="btn btn-success" @click="push">PUSH</button>
    <button type="button" class="btn btn-success" @click="replace">
      REPLACE
    </button>
    <button type="button" class="btn btn-success" @click="go">GO</button>
    <button type="button" class="btn btn-success" @click="addRoute">
      ADD ROUTE
    </button>
  </div>
</template>
<script>
export default {
  methods: {
    getRoute () {
      console.log(this.$route) // 路由的相關屬性，與進入所使用的參數 params，如 動態路由與 props 中傳入的 id
      console.log(this.$router) // 路由的相關方法，需呼叫
    },
    // push 跳頁，會產生瀏覽器的瀏覽紀錄
    push () {
      //   this.$router.push('/newPage/dynamicRouter/d416081d001f43a9')
      this.$router.push({
        name: 'About'
      })
    },
    // replace 跳頁，不會產生瀏覽器的瀏覽紀錄 ( 無法透過上一頁返回 )
    replace () {
      this.$router.replace({
        name: 'About'
      })
    },
    // go 瀏覽紀錄的操作
    go () {
      this.$router.go(-1) // 參數為返回 / 向前的頁面數
    },
    // addRoute 新增路由，即路由表結構，將創造新的路徑 ( 不會自動跳轉 )
    addRoute () {
      this.$router.addRoute({
        path: '/newAbout',
        name: 'newAbout',
        component: () =>
          import('../views/About.vue')
      })
    }
  }
}
</script>
