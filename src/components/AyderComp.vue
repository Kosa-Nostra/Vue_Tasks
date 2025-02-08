<template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
    <input v-model="newItem" type="text" placeholder="Введите текст" />
    <button @click="addItem">Добавить в список</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ["Элемент 1", "Элемент 2", "Элемент 3"], // Исходный массив
      newItem: "" // Переменная для текста из инпута
    };
  },
  methods: {
    addItem() {
      if (this.newItem.trim() !== "") { // Проверяем, что текст не пустой
        this.items.push(this.newItem); // Добавляем новый элемент в массив
        this.newItem = ""; // Очищаем инпут
      }
    }
  }
};
</script>
