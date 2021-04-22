<template>
  <section class="material">
    <h3 class="material__title">Nguyên liệu<span>4 phần ăn</span></h3>
    <section class="material__list" v-for="materialGroup in dataMaterial" >
      <h4 v-if="materialGroup.materialGroupName">{{materialGroup.materialGroupName}}</h4>
      <dl v-if="materialGroup.list.length > 0">
        <template v-for="material in materialGroup.list">
          <dt>{{material.name}}</dt><dd>{{material.size}}{{material.sizeType}}</dd>
        </template>
      </dl>
    </section>
  </section>
</template>

<script>
export default {
  name: "RecipeMaterial",
  props: {
    dataMaterial: {
      type: Array,
      required: false
    },
    dishNumber: {
      type: Number,
      required: false,
      default: 1
    },
  }
}
</script>

<style scoped>

</style>
