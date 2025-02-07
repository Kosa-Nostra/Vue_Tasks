<template>
  <div>
    <button @click="toggleParagraph">Переключить абзац</button>
    <p v-if="isParagraphVisible">Это абзац, который можно скрыть или показать.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isParagraphVisible: true // Изначальное состояние абзаца (видим)
    };
  },
  methods: {
    toggleParagraph() {
      this.isParagraphVisible = !this.isParagraphVisible; // Переключить видимость абзаца
    }
  }
}
</script>
