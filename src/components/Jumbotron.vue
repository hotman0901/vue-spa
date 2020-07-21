<template>
  <div class="jumbotron">
    <h1 class="display-4">id: {{id}}</h1>
    <h1 class="display-4">title: {{title}}</h1>
    <p class="lead">
      This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured
      content or information.
    </p>
  </div>
</template>

<script>
export default {
  name: "Jumbotron",
  props: {
    id: String,
    title: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
