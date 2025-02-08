<template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="index" @click="removeItem(index)">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ["Элемент 1", "Элемент 2", "Элемент 3"] // Исходный массив
    };
  },
  methods: {
    removeItem(index) {
      this.items.splice(index, 1); // Удаляем элемент из массива по индексу
    }
  }
};
</script>
