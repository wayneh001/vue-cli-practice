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
            to="/newPage/NamedView"
            class="list-group-item"
          >
            NamedView
          </router-link>
        </div>
      </div>
      <div class="col-8 mx-auto">
        <router-view></router-view>
      </div>
    </div>
  </div>
</template>
