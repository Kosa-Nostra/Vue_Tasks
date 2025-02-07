<template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
    <button @click="removeSecondLastItem">Удалить предпоследний элемент</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ['Элемент 1', 'Элемент 2', 'Элемент 3', 'Элемент 4'],
    };
  },
  methods: {
    removeSecondLastItem() {
      if (this.items.length > 1) {
        this.items.splice(this.items.length - 2, 1);
      }
    },
  },
};
</script>
