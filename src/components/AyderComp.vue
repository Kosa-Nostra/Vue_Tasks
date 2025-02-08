<template>
  <div>
    <input v-model.number="number" type="number" placeholder="Введите число" />
    <p>Квадрат числа: {{ squaredNumber }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: null
    };
  },
  computed: {
    squaredNumber() {
      return this.number !== null ? this.number ** 2 : "";
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
