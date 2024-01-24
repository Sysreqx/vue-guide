<template>
  <todo-list></todo-list>
  <author-list></author-list>
  <br>
  <watch-example></watch-example>
  <br>
  <list-drawings></list-drawings>
</template>

<script>
import TodoList from "@/components/TodoList.vue";
import AuthorList from "@/components/AuthorList.vue";
import WatchExample from "@/components/WatchExample.vue";
import ListDrawings from "@/components/ListDrawings.vue";

export default {
  components: {
    ListDrawings,
    TodoList,
    AuthorList,
    WatchExample
  },
}
</script>

<style scoped>

</style>