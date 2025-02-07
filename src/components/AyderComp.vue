<template>
  <div>
    <p>Цена за единицу: {{ cost }}</p>
    <p>Количество: {{ amount }}</p>
    <p>Общая стоимость: {{ price }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cost: 100,
      amount: 5
    };
  },
  computed: {
    price() {
      return this.cost * this.amount;
    }
  }
}
</script>