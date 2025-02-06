<script>
export default {
  data() {
    return {
      currentDay: "",
    };
  },
  methods: {
    getWeekday(num) {
      const days = [
        "Воскресенье", "Понедельник", "Вторник", 
        "Среда", "Четверг", "Пятница", "Суббота"
      ];
      return days[num % 7] || "Некорректное число";
    },
    showCurrentDay() {
      const today = new Date().getDay(); // Получаем номер дня (0 - Воскресенье, 6 - Суббота)
      this.currentDay = this.getWeekday(today);
    }
  },
  mounted() {
    this.showCurrentDay();
  }
};
</script>

<template>
  <div>
    <p>Сегодня: {{ currentDay }}</p>
  </div>
</template>
