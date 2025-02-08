<!-- App.vue -->
<template>
  <div>
    <h1>Данные о работнике</h1>
    <employee :func="func"></employee>
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
    func(name) {
      console.log(name);
    }
  }
};
</script>
