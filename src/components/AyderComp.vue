<template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
    <button @click="removeLastItem">Удалить последний элемент</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ['Элемент 1', 'Элемент 2', 'Элемент 3'],
    };
  },
  methods: {
    removeLastItem() {
      this.items.pop();
    },
  },
};
</script>
