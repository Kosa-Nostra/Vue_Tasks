<template>
  <p :style="{color: 'green', backgroundColor: 'yellow'}">
TEXT
  </p>
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
