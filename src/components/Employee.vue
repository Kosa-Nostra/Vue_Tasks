<!-- Employee.vue -->
<template>
	<div>
	  <span>{{ employee.name }} - {{ employee.salary }} - {{ employee.age }} лет</span>
	  <button @click="deleteEmployee">Удалить</button>
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
	methods: {
	  deleteEmployee() {
		// Испускаем событие для удаления работника
		this.$emit('delete-employee', this.index);
	  }
	}
  };
  </script>
  