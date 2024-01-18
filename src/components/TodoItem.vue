<script>
  export default {
    name: "todo-item",
    props: ['todo'],
  }
</script>

<template>
  <li>{{ todo.text }}</li>
</template>

<style scoped>

</style>