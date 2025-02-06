<template>
  <div>
    <p>{{ text }}</p>
    <button @click="changeText">Изменить текст</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: 'Начальный текст'
    };
  },
  methods: {
    changeText() {
      this.text = 'Новый текст';
    }
  }
}
</script>
