<template>
  <div>
    <p :class="{ hidden: obj.hidden }">Этот абзац может быть скрыт.</p>
    <button @click="toggleVisibility">Переключить видимость</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        hidden: true,
      },
    };
  },
  methods: {
    toggleVisibility() {
      this.obj.hidden = !this.obj.hidden;
    },
  },
};
</script>

<style>
.hidden {
  display: none;
}
</style>
