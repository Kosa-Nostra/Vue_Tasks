<template>
  <div>
    <ul>
      <li v-for="([key, value], index) in entries" :key="index">
        {{ key }} - {{ value }}
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
  computed: {
    entries() {
      return Object.entries(this.users);
    },
  },
};
</script>
