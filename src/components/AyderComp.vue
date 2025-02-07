<template>
  <div>
    <button @click="visible = true">Показать абзац</button>
    <p v-show="visible">Этот абзац был скрыт, но теперь виден.</p>
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
