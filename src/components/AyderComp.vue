<template>
  <div>
    <textarea v-model="text" placeholder="Введите текст"></textarea>
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
textarea {
  display: block;
  width: 100%;
  height: 100px;
  margin-bottom: 10px;
  padding: 5px;
  resize: vertical;
}
</style>
