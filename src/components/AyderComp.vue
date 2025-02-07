<template>
  <div>
    <ul>
      <li v-for="(value, index) in values" :key="index">{{ value }}</li>
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
    values() {
      return Object.values(this.users);
    },
  },
};
</script>
