<template>
  <div>
    <div class="row">
      <div class="col-4">
        <div class="list-group list-group-flush">
          <router-link
            to="/newPage/a"
            class="list-group-item"
          >
            元件 A
          </router-link>
          <router-link
            to="/newPage/b"
            class="list-group-item"
          >
            元件 B
          </router-link>
          <router-link
            to="/newPage/namedView"
            class="list-group-item"
          >
            具名視圖
          </router-link>
          <router-link
            to="/newPage/dynamicRouter/:id"
            class="list-group-item"
          >
            動態路由
          </router-link>
          <router-link
            to="/newPage/dynamicRouterByProps/:id"
            class="list-group-item"
          >
            動態路由與 props
          </router-link>
          <router-link
            to="/newPage/routerNavigation"
            class="list-group-item"
          >
            路由導覽
          </router-link>
        </div>
      </div>
      <div class="col-8 mx-auto">
        <router-view></router-view>
      </div>
    </div>
  </div>
</template>
