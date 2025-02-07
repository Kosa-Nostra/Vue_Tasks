<template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
    <button @click="removeFirstItem">Удалить первый элемент</button>
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
    removeFirstItem() {
      this.items.shift();
    },
  },
};
</script>
