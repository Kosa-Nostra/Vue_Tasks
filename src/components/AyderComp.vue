<template>
  <ul>
    <li v-for="(item, index) in items" :key="index">
      {{ item }}
      <p v-if="index < items.length - 1" class="divider"></p>
    </li>
  </ul>
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
