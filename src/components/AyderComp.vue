<template>
  <div>
    <ul>
      <li v-for="(item, index) in reversedItems" :key="index">{{ item }}</li>
    </ul>
    <button @click="reverseItems">Перевернуть список</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ['Элемент 1', 'Элемент 2', 'Элемент 3'],
    };
  },
  computed: {
    reversedItems() {
      return [...this.items].reverse();
    },
  },
  methods: {
    reverseItems() {
      this.items = this.reversedItems;
    },
  },
};
</script>
