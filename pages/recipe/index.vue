<template>
  <div class="container recipe">
    <h1>Danh sách món ăn</h1>
    <div class="recipe-list">
      <div class="recipe-list-item">
        <figure>
          <n-link to="/recipe/detail/">
            <div class="recipe-list-item__image">
              <img src="/images/recipe/01_01.jpg" alt="">
            </div>
            <span class="recipe-list-item__title">
            Mì hoành thánh
          </span>
          </n-link>
        </figure>
      </div>
      <div class="recipe-list-item">
        <figure>
          <a href="#">
            <div class="recipe-list-item__image">
              <img src="/images/recipe/01_01.jpg" alt="">
            </div>
            <span class="recipe-list-item__title">
            Mì hoành thánh
          </span>
          </a>
        </figure>
      </div>
      <div class="recipe-list-item">
        <figure>
          <a href="#">
            <div class="recipe-list-item__image">
              <img src="/images/recipe/01_01.jpg" alt="">
            </div>
            <span class="recipe-list-item__title">
            Mì hoành thánh
          </span>
          </a>
        </figure>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "index",
  }
</script>

<style scoped>

</style>
