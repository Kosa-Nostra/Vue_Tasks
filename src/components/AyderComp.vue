<template>
  <div>
    <input type="text" v-model="inputText" @keydown.enter="showText" placeholder="Введите текст" />
    <p v-if="submittedText">Вы ввели: {{ submittedText }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: "", // Текущий текст в инпуте
      submittedText: "" // Текст, который был отправлен
    };
  },
  methods: {
    showText() {
      this.submittedText = this.inputText; // Копируем введенный текст в переменную для отображения
      this.inputText = ""; // Очищаем инпут
    }
  }
};
</script>
