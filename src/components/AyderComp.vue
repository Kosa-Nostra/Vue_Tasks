<template>
  <div>
    <button @click.once="handleClick">Нажмите меня</button>
  </div>
</template>

<script>
export default {
  methods: {
    handleClick() {
      alert('Кнопка нажата!');
    }
  }
}
</script>
