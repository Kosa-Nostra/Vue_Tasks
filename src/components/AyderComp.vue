<template>
  <div>
    <a href="#" @click="handleClick">Нажмите на меня с зажатым Ctrl</a>
    <p v-if="messageVisible">{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      messageVisible: false, // Состояние для отображения сообщения
      message: "Вы нажали ссылку с зажатым Ctrl!" // Сообщение для вывода
    };
  },
  methods: {
    handleClick(event) {
      if (event.ctrlKey) { // Проверяем, была ли зажата клавиша Ctrl
        this.messageVisible = true; // Показываем сообщение
      }
    }
  }
};
</script>
