<script>
  export default {
    data() {
      return {
        author: {
          name: 'John Doe',
          books: [
            'Vue 2 - Advanced Guide',
            'Vue 3 - Basic Guide',
            'Vue 4 - The Mystery'
          ]
        }
      }
    },
    computed: {
      // геттер вычисляемого свойства
      publishedBooksMessage() {
        // `this` указывает на экземпляр vm
        return this.author.books.length > 0 ? 'Да' : 'Нет'
      }
    }
  }
</script>

<template>
  <div id="computed-basics">
    <p>Есть опубликованные книги:</p>
    <span>{{ publishedBooksMessage }}</span>
  </div>
</template>

<style scoped>

</style>