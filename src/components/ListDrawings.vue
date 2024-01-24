<template>
  <div>
    <ul id="array-rendering">
      <li v-for="item in items" v-bind:key="item.message">
        {{ item.message }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { message: 'Foo' },
        { message: 'Bar' }
      ]
    }
  },

}
</script>

<style scoped>

</style>