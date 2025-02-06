<template>
  <div>
    <button @click="showSquare(4)">Показать квадрат числа 4</button>
  </div>
</template>

<script>
export default {
  methods: {
    showSquare(number) {
      const square = number * number;
      alert(`Квадрат числа ${number} равен ${square}`);
    }
  }
}
</script>
