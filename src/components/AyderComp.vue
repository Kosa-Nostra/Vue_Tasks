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
	import EmployeeComp from './components/EmployeeComp.vue'
	
	export default {
		
	}
</script>
