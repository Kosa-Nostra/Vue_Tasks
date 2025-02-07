<template>
  <div>
    <ul>
      <li v-for="(item, index) in sortedItems" :key="index">{{ item }}</li>
    </ul>
    <button @click="sortItems">Сортировать</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ['Элемент 3', 'Элемент 1', 'Элемент 2'],
    };
  },
  computed: {
    sortedItems() {
      return [...this.items].sort();
    },
  },
  methods: {
    sortItems() {
      this.items = this.sortedItems;
    },
  },
};
</script>
