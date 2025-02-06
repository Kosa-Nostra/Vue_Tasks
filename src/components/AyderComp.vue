<script>
export default {
  methods: {
    getWeekday(num) {
      const days = [
        "Воскресенье", "Понедельник", "Вторник", 
        "Среда", "Четверг", "Пятница", "Суббота"
      ];
      return days[num % 7] || "Некорректное число";
    }
  }
}
</script>
<template>
	<div>
	  <p>{{ getWeekday(3) }}</p> 
	</div>
  </template>