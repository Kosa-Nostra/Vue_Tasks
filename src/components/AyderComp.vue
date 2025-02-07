<template>
  <div>
    <p v-if="isAdmin">Вы администратор.</p>
    <p v-else>Вы не администратор.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isAdmin: true // Изначальное значение свойства isAdmin
    };
  }
}
</script>
