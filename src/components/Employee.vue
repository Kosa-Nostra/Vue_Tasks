<!-- Employee.vue -->
<template>
	<div>
	  <div v-if="isEditing">
		<input v-model="editableEmployee.name" placeholder="Имя" />
		<input v-model="editableEmployee.salary" placeholder="Зарплата" type="number" />
		<input v-model="editableEmployee.age" placeholder="Возраст" type="number" />
		<button @click="saveChanges">Сохранить</button>
		<button @click="cancelEditing">Отменить</button>
	  </div>
	  <div v-else>
		<span>{{ editableEmployee.name }} - {{ editableEmployee.salary }} - {{ editableEmployee.age }} лет</span>
		<button @click="deleteEmployee">Удалить</button>
		<button @click="startEditing">Редактировать</button>
	  </div>
	</div>
  </template>
  
  <script>
  export default {
	props: {
	  employee: {
		type: Object,
		required: true
	  },
	  index: {
		type: Number,
		required: true
	  }
	},
	data() {
	  return {
		isEditing: false, // Флаг редактирования
		editableEmployee: { ...this.employee } // Создаем копию данных для редактирования
	  };
	},
	methods: {
	  // Метод для удаления работника
	  deleteEmployee() {
		this.$emit('delete-employee', this.index);
	  },
	  // Метод для начала редактирования
	  startEditing() {
		this.isEditing = true;
		this.editableEmployee = { ...this.employee }; // Создаем копию данных для редактирования
	  },
	  // Метод для отмены редактирования
	  cancelEditing() {
		this.isEditing = false;
	  },
	  // Метод для сохранения изменений
	  saveChanges() {
		this.$emit('update-employee', this.index, this.editableEmployee);
		this.isEditing = false;
	  }
	}
  };
  </script>
  