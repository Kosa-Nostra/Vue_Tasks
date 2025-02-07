<template>
  <div>
    <div v-for="(item, index) in items" :key="index">
      <p>{{ item }}</p>
      <p class="divider"></p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3],
    };
  },
};
</script>
