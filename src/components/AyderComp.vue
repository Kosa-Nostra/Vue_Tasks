<template>
  <div>
    <p v-show="isVisible">Этот абзац может быть скрыт или показан.</p>
    <button @click="isVisible = true">Показать элемент</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: false, // Изначально элемент скрыт
    };
  },
};
</script>

<style>
/* Дополнительные стили при необходимости */
</style>
