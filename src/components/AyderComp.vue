<template>
  <div>
    <ul>
      <li v-for="(value, key, index) in users" :key="index">
        {{ key }} - {{ value }} - {{ index }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: {
        user1: '100$',
        user2: '200$',
        user3: '300$',
      },
    };
  },
};
</script>
