<template>
  <div>
    <input v-model="text" placeholder="Введите текст" />
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: ""
    };
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
