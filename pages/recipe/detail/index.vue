<template>
  <div class="container recipe-detail">
    <RecipeMainVisual ></RecipeMainVisual>
    <div class="content">
      <LocalNav></LocalNav>
      <RecipeMain></RecipeMain>
    </div>
  </div>
</template>

<script>
import RecipeMainVisual from '~/components/recipe/RecipeMainVisual'
import LocalNav from '~/components/recipe/LocalNav'
import RecipeMain from '~/components/recipe/RecipeMain'
  export default {
    name: "index",
    layout: 'recipe',
    components: {
      RecipeMainVisual,
      LocalNav,
      RecipeMain
    }
  }
</script>

<style scoped>

</style>
