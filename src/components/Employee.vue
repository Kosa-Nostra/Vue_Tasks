<!-- Employee.vue -->
<template>
	<div>
	  <h2>Данные работника</h2>
	  <p>Имя: {{ name }}</p>
	  <p>Зарплата: {{ salary }}</p>
	  <p>Возраст: {{ age }}</p>
	</div>
  </template>
  
  <script>
  export default {
	props: {
	  name: {
		type: String,
		required: true
	  },
	  salary: {
		type: Number,
		required: true
	  },
	  age: {
		type: Number,
		required: true
	  }
	}
  };
  </script>
  