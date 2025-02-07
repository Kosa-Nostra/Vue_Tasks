<template>
  <div>
    <p :class="{ valid: isValid, disabled: isDisabled }">
      Этот абзац изменяет классы в зависимости от свойств.
    </p>
    <button @click="toggleValid">Переключить валидность</button>
    <button @click="toggleDisabled">Переключить доступность</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isValid: true,
      isDisabled: true,
    };
  },
  methods: {
    toggleValid() {
      this.isValid = !this.isValid;
    },
    toggleDisabled() {
      this.isDisabled = !this.isDisabled;
    },
  },
};
</script>

<style>
.valid {
  color: green;
  font-weight: bold;
}

.disabled {
  color: gray;
  text-decoration: line-through;
}
</style>
