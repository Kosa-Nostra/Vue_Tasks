<template>
  <div>
    <input v-model.number="number1" type="number" placeholder="Введите первое число" />
    <input v-model.number="number2" type="number" placeholder="Введите второе число" />
    <button @click="calculateSum">Посчитать сумму</button>
    <p v-if="sum !== null">Сумма: {{ sum }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number1: null,
      number2: null,
      sum: null
    };
  },
  methods: {
    calculateSum() {
      this.sum = (this.number1 ?? 0) + (this.number2 ?? 0);
    }
  }
};
</script>

<style scoped>
input, button {
  display: block;
  margin-bottom: 10px;
  padding: 5px;
}
</style>
