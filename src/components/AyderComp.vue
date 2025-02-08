<template>
  <div>
    <h3>Выберите день, месяц и год:</h3>

    <select v-model="selectedDay">
      <option disabled value="">День</option>
      <option v-for="day in days" :key="day" :value="day">{{ day }}</option>
    </select>

    <select v-model="selectedMonth">
      <option disabled value="">Месяц</option>
      <option v-for="(month, index) in months" :key="index" :value="index + 1">{{ month }}</option>
    </select>

    <select v-model="selectedYear">
      <option disabled value="">Год</option>
      <option v-for="year in years" :key="year" :value="year">{{ year }}</option>
    </select>

    <div v-if="selectedDay && selectedMonth && selectedYear">
      <p>Вы выбрали: {{ selectedDay }} {{ months[selectedMonth - 1] }} {{ selectedYear }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    const today = new Date();
    const currentDay = today.getDate();
    const currentMonth = today.getMonth() + 1; // Месяцы начинаются с 0
    const currentYear = today.getFullYear();

    return {
      selectedDay: currentDay, // Устанавливаем текущий день
      selectedMonth: currentMonth, // Устанавливаем текущий месяц
      selectedYear: currentYear, // Устанавливаем текущий год
      days: Array.from({ length: 31 }, (_, i) => i + 1), // Массив дней от 1 до 31
      months: [
        "Январь", "Февраль", "Март", "Апрель", "Май", "Июнь",
        "Июль", "Август", "Сентябрь", "Октябрь", "Ноябрь", "Декабрь"
      ], // Массив месяцев
      years: Array.from({ length: 101 }, (_, i) => 1900 + i) // Массив годов с 1900 по 2000
    };
  }
};
</script>
