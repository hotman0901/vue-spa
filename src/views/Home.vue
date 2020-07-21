<template>
  <div class="home">
    <Nav />
    <Slide />
    <div class="form-group">
      <label for="exampleFormControlSelect1">Example select</label>
      <select class="form-control" v-model="option.value">
        <option value>請選擇</option>
        <option v-for="opt in option.list" :key="opt">{{ opt }}</option>
      </select>

      選到號碼：{{ option.value }}
      <!-- 依照選單號碼 render -->
      <div v-if="option.value !== ''">
        <Jumbotron :id="option.value" :title="`我是標題${option.value}`" />
      </div>
      <div v-else>
        <h1>沒選</h1>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Nav from "@/components/Nav.vue"
import Slide from "@/components/Slide.vue"
import Jumbotron from "@/components/Jumbotron.vue"


export default {
  name: "home",
  components: {
    Nav,
    Slide,
    Jumbotron
  },
  data() {
    return {
      option: {
        value: "",
        list: [1, 2, 3, 4, 5]
      }
    }
  }
}
</script>
