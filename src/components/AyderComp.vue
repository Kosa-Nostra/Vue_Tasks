<template>
  <div>
    <div v-for="(item, index) in items" :key="index">
      {{ item * item }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3, 4, 5]
    };
  }
}
</script>
