<!-- EmployeeList.vue -->
<template>
	<ul>
	  <li v-for="(item, index) in items" :key="index">{{ item }}</li>
	</ul>
  </template>
  
  <script>
  export default {
	props: {
	  items: Array
	}
  };
  </script>
  