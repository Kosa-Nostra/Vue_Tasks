<!-- Employee.vue -->
<template>
	<div>
	  <button @click="sendNameToParent">Отправить имя родителю</button>
	</div>
  </template>
  
  <script>
  export default {
	props: {
	  func: {
		type: Function,
		required: true
	  }
	},
	methods: {
	  sendNameToParent() {
		// Вызов метода родителя, передаем имя работника
		this.func('Иван Иванов');
	  }
	}
  };
  </script>
  