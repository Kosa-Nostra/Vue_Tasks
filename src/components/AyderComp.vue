<template>
  <div>
    <button @click="hideParagraphs">Скрыть абзацы</button>
    <p v-if="!areParagraphsHidden">Первый абзац</p>
    <p v-if="!areParagraphsHidden">Второй абзац</p>
    <p v-if="!areParagraphsHidden">Третий абзац</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      areParagraphsHidden: false // Изначальное состояние абзацев (видимы)
    };
  },
  methods: {
    hideParagraphs() {
      this.areParagraphsHidden = true; // Скрыть абзацы
    }
  }
}
</script>
