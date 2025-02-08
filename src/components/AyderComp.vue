<template>
  <div>
    <textarea v-model="text" placeholder="Введите текст"></textarea>
    <button @click="splitText">Разбить на слова</button>
    <ul v-if="words.length">
      <li v-for="(word, index) in words" :key="index">{{ word }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: "",
      words: []
    };
  },
  methods: {
    splitText() {
      this.words = this.text.trim().split(/\s+/).filter(word => word);
    }
  }
};
</script>

<style scoped>
textarea, button {
  display: block;
  width: 100%;
  margin-bottom: 10px;
  padding: 5px;
  resize: vertical;
}
</style>
