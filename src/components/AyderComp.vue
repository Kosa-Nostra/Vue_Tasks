<template>
  <p v-if="!hidden">text</p>
</template>

<script>
export default {
  data() {
    return {
      hidden: true // Изначальное значение свойства hidden
    };
  }
}
</script>
