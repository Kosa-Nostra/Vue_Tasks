<template>
  <div>
    <button @click="showSquare(2)">Показать квадрат числа 2</button>
    <button @click="showSquare(3)">Показать квадрат числа 3</button>
  </div>
</template>

<script>
export default {
  methods: {
    showSquare(number) {
      const square = number ** 2;
      alert(`Квадрат числа ${number} равен ${square}`);
    }
  }
}
</script>
