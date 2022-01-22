<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div class="container">
      <div class="row">
        <div class="col">
          <Card></Card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue' // ＠ 為 src 縮寫
export default {
  components: {
    Card
  }
}
// 引入 components 同時必須 export default，並使用 components 物件裝載引入時宣告的參數 ( Card )
</script>
