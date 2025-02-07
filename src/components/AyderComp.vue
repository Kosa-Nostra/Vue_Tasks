<template>
  <div>
    <p v-show="isVisible">Этот абзац может быть скрыт или показан.</p>
    <button @click="isVisible = false">Скрыть элемент</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: true, // Изначально элемент видим
    };
  },
};
</script>

<style>
/* Дополнительные стили при необходимости */
</style>
