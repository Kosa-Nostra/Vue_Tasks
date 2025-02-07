<template>
  <div>
    <p v-if="visible">Первый абзац отображается, когда visible = true.</p>
    <p v-else>Второй абзац отображается, когда visible = false.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: true // Изначальное значение свойства visible
    };
  }
}
</script>
