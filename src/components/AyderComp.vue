<template>
  <div>
    <input type="checkbox" v-model="isChecked" /> Показать абзац
    <p v-if="isChecked">Этот абзац будет показан, если чекбокс отмечен.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isChecked: false
    };
  }
};
</script>
