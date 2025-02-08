<!-- Employee.vue -->
<template>
	<tr>
	  <td>{{ name }}</td>
	  <td>{{ salary }}</td>
	  <td>{{ age }}</td>
	</tr>
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
  