<template>
  <div>
    <input v-model.number="number" type="number" placeholder="Введите число" />
    <button @click="calculateSqrt">Вычислить корень</button>
    <p v-if="sqrtResult !== null">Квадратный корень: {{ sqrtResult }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: null,
      sqrtResult: null
    };
  },
  methods: {
    calculateSqrt() {
      if (this.number !== null && this.number >= 0) {
        this.sqrtResult = Math.sqrt(this.number).toFixed(2); // округление до 2 знаков
      } else {
        this.sqrtResult = "Некорректный ввод";
      }
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
