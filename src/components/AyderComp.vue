<template>
  <div>
    <a href="#" @mousedown="handleMouseDown">Нажмите на меня мышью</a>
    <p v-if="clickedButton">Вы нажали: {{ clickedButton }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      clickedButton: "" // Переменная для хранения текста, который будет отображаться
    };
  },
  methods: {
    handleMouseDown(event) {
      // Проверяем, какая кнопка была нажата
      if (event.button === 0) {
        this.clickedButton = "left"; // Левая кнопка мыши
      } else if (event.button === 1) {
        this.clickedButton = "middle"; // Средняя кнопка мыши
      } else if (event.button === 2) {
        this.clickedButton = "right"; // Правая кнопка мыши
      }
    }
  }
};
</script>
