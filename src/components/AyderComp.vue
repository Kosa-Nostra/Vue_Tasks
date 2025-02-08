<!-- App.vue -->
<template>
  <div>
    <h1>Данные о работнике</h1>
    <employee 
      :func="func" 
      :name="worker.name" 
      :salary="worker.salary"
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
      worker: {
        name: 'Иван Иванов',
        salary: 50000
      }
    };
  },
  methods: {
    func(name, salary) {
      console.log(name, salary);  // Выводит имя и зарплату работника в консоль
    }
  }
};
</script>
