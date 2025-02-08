<!-- App.vue -->
<template>
  <div>
    <h1>Список элементов</h1>
    <employee-list :items="items"></employee-list>
  </div>
</template>

<script>
// Импортируем дочерний компонент
import EmployeeList from './EmployeeList.vue';

export default {
  components: {
    EmployeeList
  },
  data() {
    return {
      items: ['Элемент 1', 'Элемент 2', 'Элемент 3', 'Элемент 4']
    };
  }
};
</script>
