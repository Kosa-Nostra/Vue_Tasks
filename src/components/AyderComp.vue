
<template>
  <div>
    <h1>Список работников</h1>
    <EmployeeForm @add-employee="addNewEmployee" />
    <div v-for="(user, index) in users" :key="user.id">
      <Employee 
        :employee="user" 
        :index="index" 
        @delete-employee="removeUser"
        @update-employee="updateUser"
      />
    </div>
  </div>
</template>

<script>
// Импортируем компоненты Employee и EmployeeForm
import Employee from './Employee.vue';
import EmployeeForm from './EmployeeForm.vue';

export default {
  components: {
    Employee,
    EmployeeForm
  },
  data() {
    return {
      users: [
        { id: 1, name: 'name1', salary: 100, age: 30 },
        { id: 2, name: 'name2', salary: 200, age: 40 },
        { id: 3, name: 'name3', salary: 300, age: 50 }
      ]
    };
  },
  methods: {
    // Метод для удаления работника
    removeUser(index) {
      this.users.splice(index, 1);  // Удаляем работника из списка
    },
    // Метод для обновления данных работника
    updateUser(index, updatedEmployee) {
      this.$set(this.users, index, updatedEmployee);  // Обновляем данные работника по индексу
    },
    // Метод для добавления нового работника
    addNewEmployee(newEmployee) {
      const newId = this.users.length ? Math.max(...this.users.map(user => user.id)) + 1 : 1;
      this.users.push({ ...newEmployee, id: newId }); // Добавляем нового работника в список
    }
  }
};
</script>
