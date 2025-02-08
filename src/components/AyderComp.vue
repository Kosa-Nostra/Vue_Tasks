<template>
  <div>
    <h3>Выберите день недели:</h3>
    <select v-model="selectedDay">
      <option value="Понедельник">Понедельник</option>
      <option value="Вторник">Вторник</option>
      <option value="Среда">Среда</option>
      <option value="Четверг">Четверг</option>
      <option value="Пятница">Пятница</option>
      <option value="Суббота">Суббота</option>
      <option value="Воскресенье">Воскресенье</option>
    </select>

    <div v-if="selectedDay">
      <p>Вы выбрали: {{ selectedDay }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedDay: "" // Переменная для хранения выбранного дня недели
    };
  }
};
</script>
