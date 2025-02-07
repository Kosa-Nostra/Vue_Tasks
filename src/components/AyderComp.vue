<template>
  <div>
    <a href="https://example.com" @click.prevent="handleClick">Нажмите здесь</a>
  </div>
</template>

<script>
export default {
  methods: {
    handleClick() {
      // Логика, выполняемая при клике на ссылку
      console.log('Ссылка была нажата, но переход отменен.');
    }
  }
}
</script>
