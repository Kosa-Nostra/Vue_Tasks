<!-- EmployeeForm.vue -->
<template>
    <div>
      <h2>Добавить нового работника</h2>
      <form @submit.prevent="addEmployee">
        <input v-model="newEmployee.name" placeholder="Имя" required />
        <input v-model="newEmployee.salary" type="number" placeholder="Зарплата" required />
        <input v-model="newEmployee.age" type="number" placeholder="Возраст" required />
        <button type="submit">Добавить</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        newEmployee: {
          name: '',
          salary: '',
          age: ''
        }
      };
    },
    methods: {
      addEmployee() {
        // Испускаем событие с новыми данными работника
        this.$emit('add-employee', { ...this.newEmployee });
        
        // Очищаем форму после добавления
        this.newEmployee.name = '';
        this.newEmployee.salary = '';
        this.newEmployee.age = '';
      }
    }
  };
  </script>
  