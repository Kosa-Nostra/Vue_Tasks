<template>
  <div>
    <p v-if="isVisible">Этот абзац отображается, когда isVisible = true.</p>
    <button v-if="!isVisible" @click="toggleVisibility">Показать абзац</button>
    <button v-else @click="toggleVisibility">Скрыть абзац</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: false // Изначально абзац скрыт
    };
  },
  methods: {
    toggleVisibility() {
      this.isVisible = !this.isVisible;
    }
  }
}
</script>
