<!-- App.vue -->
<template>
  <div>
    <h1>Список работников</h1>
    <div v-for="(user, index) in users" :key="user.id">
      <!-- Передаем данные работника в компонент Employee -->
      <Employee 
        :employee="user" 
        :index="index" 
        @delete-employee="removeUser"
      />
    </div>
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
      users: [
        { id: 1, name: 'name1', salary: 100, age: 30 },
        { id: 2, name: 'name2', salary: 200, age: 40 },
        { id: 3, name: 'name3', salary: 300, age: 50 }
      ]
    };
  },
  methods: {
    removeUser(index) {
      this.users.splice(index, 1);  // Удаляем работника из списка
    }
  }
};
</script>
