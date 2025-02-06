<template>
  <div>
    <p>{{ text }}</p>
    <button @click="updateText('Первое значение')">Установить первое значение</button>
    <button @click="updateText('Второе значение')">Установить второе значение</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: 'Начальное значение'
    };
  },
  methods: {
    updateText(newText) {
      this.text = newText;
    }
  }
}
</script>
