<template>
  <div>
    <p v-if="day === 'Понедельник'">Понедельник</p>
    <p v-if="day === 'Вторник'">Вторник</p>
    <p v-if="day === 'Среда'">Среда</p>
    <p v-if="day === 'Четверг'">Четверг</p>
    <p v-if="day === 'Пятница'">Пятница</p>
    <p v-if="day === 'Суббота'">Суббота</p>
    <p v-if="day === 'Воскресенье'">Воскресенье</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      day: 'Понедельник' // Изначальное значение свойства day
    };
  }
}
</script>
