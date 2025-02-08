<template>
  <div>
    <input type="text" v-bind:disabled="!isChecked" placeholder="Введите текст" />
    <label>
      <input type="checkbox" v-model="isChecked" />
      Инпут активен
    </label>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isChecked: false // Состояние чекбокса: если true — инпут активен, если false — заблокирован
    };
  }
};
</script>
