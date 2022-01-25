<template>
  <h4>命名視圖</h4>
  <ul class="nav nav-pills nav-fill mt-5">
    <li class="nav-item">
      <router-link
        to="/newPage/NamedView/c2a"
        class="nav-link"
      >
        C to A
      </router-link>
    </li>
    <li class="nav-item">
      <router-link
        to="/newPage/NamedView/a2b"
        class="nav-link"
      >
        A to B
      </router-link>
    </li>
  </ul>
  <div class="row mt-5">
    <div class="col-6">
      <router-view name="left"></router-view>
    </div>
    <div class="col-6">
      <router-view name="right"></router-view>
    </div>
  </div>
</template>
