<template>
  <div>
    <input v-model="text" placeholder="Введите текст" />
    <p>{{ upperText }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: ""
    };
  },
  computed: {
    upperText() {
      return this.text.toUpperCase();
    }
  }
};
</script>

<style scoped>
input {
  display: block;
  margin-bottom: 10px;
  padding: 5px;
}
</style>
