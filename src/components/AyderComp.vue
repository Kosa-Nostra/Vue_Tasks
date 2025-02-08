<template>
  <div>
    <table border="1">
      <thead>
        <tr>
          <th>ID</th>
          <th>Name</th>
          <th>Salary</th>
          <th>Age</th>
          <th>Actions</th> <!-- Колонка для действий -->
        </tr>
      </thead>
      <tbody>
        <tr v-for="(user, index) in users" :key="user.id">
          <td>{{ user.id }}</td>
          <td>
            <input v-if="user.isEditing" v-model="user.name" />
            <span v-else>{{ user.name }}</span>
          </td>
          <td>
            <input v-if="user.isEditing" v-model="user.salary" />
            <span v-else>{{ user.salary }}</span>
          </td>
          <td>
            <input v-if="user.isEditing" v-model="user.age" />
            <span v-else>{{ user.age }}</span>
          </td>
          <td>
            <a href="#" @click="removeUser(index)">Удалить</a>
            <a href="#" @click="toggleEdit(index)">
              {{ user.isEditing ? 'Сохранить' : 'Редактировать' }}
            </a>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { id: 1, name: 'name1', salary: 100, age: 30, isEditing: false },
        { id: 2, name: 'name2', salary: 200, age: 40, isEditing: false },
        { id: 3, name: 'name3', salary: 300, age: 50, isEditing: false },
      ]
    };
  },
  methods: {
    removeUser(index) {
      this.users.splice(index, 1); // Удаляем пользователя по индексу
    },
    toggleEdit(index) {
      const user = this.users[index];
      user.isEditing = !user.isEditing; // Переключаем режим редактирования
    }
  }
};
</script>
