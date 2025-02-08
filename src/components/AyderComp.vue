<!-- App.vue -->
<template>
  <div>
    <h1>Пример передачи функций в дочерний компонент</h1>
    <employee
      :onButtonClick1="handleButtonClick1"
      :onButtonClick2="handleButtonClick2"
    ></employee>
  </div>
</template>

<script>
// Импортируем компонент Employee
import Employee from './Employee.vue';

export default {
  components: {
    Employee
  },
  methods: {
    handleButtonClick1() {
      alert('Кнопка 1 нажата');
    },
    handleButtonClick2() {
      alert('Кнопка 2 нажата');
    }
  }
};
</script>
