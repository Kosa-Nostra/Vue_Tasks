<template>
  <div>
    <input type="text" v-bind:disabled="isDisabled" placeholder="Введите текст" />
    <button @click="toggleInput">{{ isDisabled ? 'Разблокировать' : 'Заблокировать' }}</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isDisabled: false // Состояние инпута: заблокирован или нет
    };
  },
  methods: {
    toggleInput() {
      this.isDisabled = !this.isDisabled; // Переключаем состояние
    }
  }
};
</script>
