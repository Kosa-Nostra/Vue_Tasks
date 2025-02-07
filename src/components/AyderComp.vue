<template>
  <div>
    <p v-for="number in numbers" :key="number">{{ number }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      numbers: Array.from({ length: 30 }, (_, index) => index + 1),
    };
  },
};
</script>
