<!-- App.vue -->
<template>
  <div>
    <h1>Список работников</h1>
    <table border="1">
      <thead>
        <tr>
          <th>Имя</th>
          <th>Зарплата</th>
          <th>Возраст</th>
        </tr>
      </thead>
      <tbody>
        <!-- Перебираем массив users и передаем данные в компонент Employee -->
        <employee
          v-for="user in users"
          :key="user.id"
          :name="user.name"
          :salary="user.salary"
          :age="user.age"
        ></employee>
      </tbody>
    </table>
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
        {
          id: 1,
          name: 'name1',
          salary: 100,
          age: 30
        },
        {
          id: 2,
          name: 'name2',
          salary: 200,
          age: 40
        },
        {
          id: 3,
          name: 'name3',
          salary: 300,
          age: 50
        }
      ]
    };
  }
};
</script>
