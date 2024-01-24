<template>
  <div id="watch-example">
    <p>
      Задайте вопрос, на который можно ответить «да» или «нет»:
      <input v-model="question" />
    </p>
    <p>{{ answer }}</p>
  </div>
</template>

<script>
import { vueHead } from 'vue-head';

export default {
  mixins: [vueHead],
  head: {
    script: [
      {
        src: 'https://cdn.example.com/your-script.js',
        async: true
      }
    ]
  },
  data() {
    return {
      question: '',
      answer: 'Вопросы обычно заканчиваются вопросительным знаком. ;-)',

    }
  },
  watch: {
    // при каждом изменении `question` эта функция будет запускаться
    question(newQuestion) {
      if (newQuestion.indexOf('?') > -1) {
        this.getAnswer()
      }
    }
  },
  methods: {
    // getAnswer() {
    //   this.answer = 'Думаю...';
    //   axios
    //       .get('https://yesno.wtf/api')
    //       .then(response => {
    //         this.answer = response.data.answer
    //       })
    //       .catch(error => {
    //         this.answer = 'Ошибка! Нет доступа к API. ' + error
    //       })
    // }
  }
}
</script>

<style scoped>

</style>
