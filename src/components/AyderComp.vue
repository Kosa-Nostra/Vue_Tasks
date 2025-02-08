<template>
  <div>
    <h3>В каком городе вы живете?</h3>
    <select v-model="city">
      <option value="Москва">Москва</option>
      <option value="Санкт-Петербург">Санкт-Петербург</option>
      <option value="Новосибирск">Новосибирск</option>
      <option value="Екатеринбург">Екатеринбург</option>
    </select>

    <div v-if="city">
      <p>Вы живете в городе: {{ city }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      city: "" // Переменная для хранения выбранного города
    };
  }
};
</script>
