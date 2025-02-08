<!-- Employee.vue -->
<template>
	<tr>
	  <td>{{ firstName }}</td>
	  <td>{{ lastName }}</td>
	  <td>{{ age }}</td>
	  <td>
		<input v-if="isEditing" v-model="firstName" />
		<input v-if="isEditing" v-model="lastName" />
		<input v-if="isEditing" v-model="age" />
		<span v-else>{{ firstName }} {{ lastName }} - {{ age }} лет</span>
	  </td>
	  <td>
		<a href="#" @click="removeUser">Удалить</a>
		<a href="#" @click="toggleEdit">{{ isEditing ? 'Сохранить' : 'Редактировать' }}</a>
	  </td>
	</tr>
  </template>
  
  <script>
  export default {
	props: {
	  firstName: String,
	  lastName: String,
	  age: Number,
	  index: Number,
	  isEditing: Boolean
	},
	methods: {
	  removeUser() {
		this.$emit('remove', this.index); // Отправляем событие удаления
	  },
	  toggleEdit() {
		this.$emit('toggle-edit', this.index); // Переключаем режим редактирования
	  }
	}
  };
  </script>
  