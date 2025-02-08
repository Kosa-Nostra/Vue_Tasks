<!-- Employee.vue -->
<template>
	<div>
	  <button @click="onButtonClick1">Нажми кнопку 1</button>
	  <button @click="onButtonClick2">Нажми кнопку 2</button>
	</div>
  </template>
  
  <script>
  export default {
	props: {
	  onButtonClick1: {
		type: Function,
		required: true
	  },
	  onButtonClick2: {
		type: Function,
		required: true
	  }
	}
  };
  </script>
  