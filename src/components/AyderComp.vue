<template>
  <div>
    <p :class="classObject">Этот абзац может быть активным или невалидным.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      classObject: {
        active: true,
        valid: false,
      },
    };
  },
};
</script>

<style>
.active {
  color: green;
  font-weight: bold;
}

.valid {
  text-decoration: underline;
}
</style>
