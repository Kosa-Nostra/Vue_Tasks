<template>
  <div>
    <input v-model="fullName" type="text" placeholder="Введите ФИО" />
    <button @click="splitFullName">Разделить ФИО</button>
    <p v-if="lastName">Фамилия: {{ lastName }}</p>
    <p v-if="firstName">Имя: {{ firstName }}</p>
    <p v-if="middleName">Отчество: {{ middleName }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fullName: "",
      lastName: "",
      firstName: "",
      middleName: ""
    };
  },
  methods: {
    splitFullName() {
      const parts = this.fullName.trim().split(" ");
      this.lastName = parts[0] || "";
      this.firstName = parts[1] || "";
      this.middleName = parts[2] || "";
    }
  }
};
</script>

<style scoped>
input, button {
  display: block;
  margin-bottom: 10px;
  padding: 5px;
}
</style>
