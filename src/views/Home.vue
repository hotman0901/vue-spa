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
      <div v-if="option.value === '1'">
        <div class="jumbotron">
          <h1 class="display-4">render 1</h1>
          <p class="lead">
            This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured
            content or information.
          </p>
        </div>
      </div>
      <div v-else-if="option.value === '2'">
        <div class="jumbotron">
          <h1 class="display-4">render 2</h1>
          <p class="lead">
            This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured
            content or information.
          </p>
        </div>
      </div>
      <div v-else-if="option.value === '3'">
        <div class="jumbotron">
          <h1 class="display-4">render 3</h1>
          <p class="lead">
            This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured
            content or information.
          </p>
        </div>
      </div>
      <div v-else-if="option.value === '4'">
        <div class="jumbotron">
          <h1 class="display-4">render 4</h1>
          <p class="lead">
            This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured
            content or information.
          </p>
        </div>
      </div>
      <div v-else-if="option.value === '5'">
        <div class="jumbotron">
          <h1 class="display-4">render 5</h1>
          <p class="lead">
            This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured
            content or information.
          </p>
        </div>
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

export default {
  name: "home",
  components: {
    Nav,
    Slide
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
