<template>
  <div>
    <p v-for="(item, index) in positiveItems" :key="index">{{ item }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, -2, 3, -4, 5],
    };
  },
  computed: {
    positiveItems() {
      return this.items.filter(item => item > 0);
    },
  },
};
</script>
