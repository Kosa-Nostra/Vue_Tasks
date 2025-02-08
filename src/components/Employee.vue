<!-- Employee.vue -->
<template>
	<div>
	  <button @click="sendDataToParent">Отправить данные родителю</button>
	</div>
  </template>
  
  <script>
  export default {
	props: {
	  func: {
		type: Function,
		required: true
	  },
	  name: {
		type: String,
		required: true
	  },
	  salary: {
		type: Number,
		required: true
	  }
	},
	methods: {
	  sendDataToParent() {
		// Вызов метода родителя, передаем имя и зарплату
		this.func(this.name, this.salary);
	  }
	}
  };
  </script>
  