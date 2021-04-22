<template>
  <div>
    <section class="recipe">
      <div class="recipe__description">
        <h2 class="recipe__title">{{recipeData["title"]}}</h2>
        <p v-html="recipeData.description"></p>
      </div>
    </section>
    <RecipeMaterial :dataMaterial='recipeData["material"]' :dishNumber="recipeData['dishNumber']"></RecipeMaterial>
    <section class="cooking">
      <h3 class="cooking__title">Cách làm<span v-if='recipeData.cookingTime'>Thời gian {{recipeData.cookingTime}} phút</span></h3>
      <ol class="cooking__list">
        <li v-for="step in recipeData.cooking">
          <span class="cooking__list-image" v-if="step.image"><img :src="step.image" alt=""></span>
          <span v-if="step.text" class="cooking__list-description">{{step.text}}</span>
        </li>
      </ol>
    </section>
  </div>
</template>

<script>
import RecipeMaterial from '~/components/recipe/RecipeMaterial'
export default {
  name: "RecipeMain",
  components: {
    RecipeMaterial
  },
  data() {
    return {
      recipeData: {
        id: 0,
        title: 'Mì Hoành Thánh',
        description: `Mì Hoành Thánh (mì vằn thắn). Viên hoành thánh còn được gọi là sủi cảo, làm từ thịt heo, hải sản, rau băm nhỏ cuộn bằng vỏ bột mì. <br>
        Mỗi lần nấu lại nhớ đến tô hủ tiếu "thịt chuột" trứ danh ở Sài Gòn. Nhớ mỗi lần mưa to quá trời, tấp vô quán quen kêu tô hủ tiếu hoành thánh khô xịt chút tương, bỏ miếng ớt xanh trộn đều lên rồi kệ mưa hắt vô chân, kệ mấy con chuột gần đó chạy vòng vòng, kệ hết mấy ánh đèn nhấp nháy xa hoa của những quán ăn ngoài kia... và cho đây là tô hủ tiếu ngon nhứt đời.`,
        dishNumber: 4,
        material: [
          {
            materialGroupName: '',
            list:[
              { name: 'Thịt nạc xay', size: 250, sizeType: 'g' },
              { name: 'Tôm', size: 100, sizeType: 'g'},
              { name: 'Hành khô', size: 50, sizeType: 'g'},
              { name: 'Muối', size: 0.5 , sizeType: 'mcf'},
              { name: 'Nước mắm', size: 1, sizeType: 'mcf'},
              { name: 'Đường', size: 2, sizeType: 'mcf'},
              { name: 'Hạt tiêu'},
              { name: 'Nấm hương', size: 10, sizeType: 'g'},
              { name: 'Hẹ'},
              { name: 'Vỏ sủi cảo', size: 40, sizeType: 'lá'},
              { name: 'Mỳ tươi', size: 4, sizeType: 'vắt'},
            ]
          },
          {
            materialGroupName: '＜Nước dùng＞',
            list:[
              { name: 'Đầu tôm, vỏ tôm sau khi bóc'},
              { name: 'Sườn heo non'},
              { name: 'Hành tây', sizeType: 'nửa củ'},
              { name: 'Hạt tiêu sọ, hạt ngò', size: 1 , sizeType: 'mcf'},
            ]
          }
        ],
        cookingTime: 40,
        cooking: [
          {
            text: 'Đầu tôm, vỏ tôm, tiêu sọ, hạt ngò, hành tây cho vào túi vải bỏ vào nồi nước ninh cùng xương heo, cho một chút muối. Ninh nhỏ lửa.',
            image: ''
          },
          {
            text: 'Để phần nhân tôm dai dòn hơn, sau khi sơ chế hãy nhào đập để tôm được nát ra. Sau đó trộn với thịt xay, hành khô băm nhỏ, chút muối, nước mắm, đường và hạt tiêu.',
            image: ''
          },
          {
            text: 'Lấy 1 thìa nhân muỗng cà phê để giữa miếng vỏ sủi và miết nước viền mép trong của sủi và gập lại theo hình. ',
            image: '/images/recipe/01_06.jpg'
          },
          {
            text: 'Nấu một nồi nước, khi sôi cho từ từ sủi cảo vào, khi nào nổi lên thì vớt ra, thêm một lớp dầu mỏng để không bị dính.',
            image: ''
          },
          {
            text: 'Trụng mì tươi khoảng 2 phút sau đó thêm hẹ, có thể ăn không hoành thánh thành món sủi cảo ',
            image: ''
          }
        ]
      }
    }
  },
}
</script>

<style scoped>

</style>
