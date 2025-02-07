<template>
  <div>
    <button @click="visible = true">Показать абзац</button>
    <button @click="visible = false">Скрыть абзац</button>
    <p v-show="visible">Этот абзац можно показать или скрыть.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: false // Изначально абзац скрыт
    };
  }
}
</script>
