<template>
  <div>
    <p>Цена за единицу: {{ cost }}</p>
    <p>Количество: {{ amount }}</p>
    <p>Общая стоимость: {{ price }}</p>
    <button @click="changeCost">Изменить цену</button>
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
  },
  methods: {
    changeCost() {
      this.cost = 150; // Новое значение для cost
    }
  }
}
</script>
