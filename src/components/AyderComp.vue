<template>
  <div>
    <ul>
      <li v-for="(item, index) in arr" :key="index">{{ index }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: ['x', 'y', 'z']
    };
  }
}
</script>
