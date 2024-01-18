<template>
  <div id="todo-list-app">
    <ol>
      <!--
        Теперь можно передавать каждому компоненту todo-item объект с информацией
        о задаче, который может динамически изменяться. Также каждому компоненту
        определяем "key", назначение которого разберём далее в руководстве.
      -->
      <todo-item
          v-for="item in groceryList"
          v-bind:todo="item"
          v-bind:key="item.id"
      ></todo-item>
    </ol>
  </div>
</template>

<script>

import TodoItem from "@/components/TodoItem.vue";

export default {
  name: "todo-list",
  components: {TodoItem},

  data() {
    return {
      groceryList: [
        { id: 0, text: 'Vegetables' },
        { id: 1, text: 'Cheese' },
        { id: 2, text: 'Whatever else humans are supposed to eat' }
      ]
    }
  }
}
</script>

<style scoped>

</style>