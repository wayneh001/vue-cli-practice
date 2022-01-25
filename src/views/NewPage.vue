<template>
  <div>
    <div class="row">
      <div class="col-4">
        <div class="list-group">
          <router-link
            to="/newPage/a"
            class="list-group-item list-group-item-action"
            aria-current="true"
          >
            元件 A
          </router-link>
          <router-link
            to="/newPage/b"
            class="list-group-item list-group-item-action"
            aria-current="true"
          >
            元件 B
          </router-link>
        </div>
      </div>
      <div class="col-8">
        <router-view></router-view>
      </div>
    </div>
  </div>
</template>
