<template>
  <figure class="main-visual">
    <ul class="main-visual-list">
      <li>
        <img src="/images/recipe/01_01.jpg" alt="">
      </li>
      <li>
        <img src="/images/recipe/01_03.jpg" alt="">
      </li>
      <li>
        <img src="/images/recipe/01_02.jpg" alt="">
      </li>
      <li>
        <img src="/images/recipe/01_05.jpg" alt="">
      </li>
    </ul>
    <carousel
      class="carousel"
      :per-page="1"
      :autoplay="true"
      :loop="true"
      :controls="true"
      :paginationEnabled="false"
      :autoplay-timeout="4000">
      <slide>
        <img src="/images/recipe/01_01.jpg" />
      </slide>
      <slide>
        <img src="/images/recipe/01_03.jpg" />
      </slide>
      <slide>
        <img src="/images/recipe/01_02.jpg" />
      </slide>
      <slide>
        <img src="/images/recipe/01_05.jpg" />
      </slide>
    </carousel>
  </figure>
</template>

<script>
import Carousel from 'vue-carousel/src/Carousel.vue'
import Slide from 'vue-carousel/src/Slide.vue'
export default {
  name: "RecipeMainVisual",
  components: {
    Carousel,
    Slide
  }
}
</script>

<style scoped>

</style>
