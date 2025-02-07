<template>
  <div>
    <p v-show="isVisible">Этот абзац может быть скрыт или показан.</p>
    <button @click="toggleVisibility">
      {{ isVisible ? 'Скрыть' : 'Показать' }} элемент
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: true, // Изначально элемент видим
    };
  },
  methods: {
    toggleVisibility() {
      this.isVisible = !this.isVisible;
    },
  },
};
</script>

<style>
/* Дополнительные стили при необходимости */
</style>
