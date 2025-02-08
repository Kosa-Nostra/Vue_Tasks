<!-- App.vue -->
<template>
  <div>
    <h1>Данные о работнике</h1>
    <employee 
      :name="employee.name"
      :salary="employee.salary"
      :age="employee.age"
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
  data() {
    return {
      employee: {
        name: 'Иван Иванов',
        salary: 50000,
        age: 30
      }
    };
  }
};
</script>
