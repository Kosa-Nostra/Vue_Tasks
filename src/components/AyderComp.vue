<template>
  <div>
    <h3>Какой язык для вас родной?</h3>
    <label>
      <input type="radio" value="Русский" v-model="nativeLanguage" /> Русский
    </label>
    <label>
      <input type="radio" value="Английский" v-model="nativeLanguage" /> Английский
    </label>
    <label>
      <input type="radio" value="Испанский" v-model="nativeLanguage" /> Испанский
    </label>
    <label>
      <input type="radio" value="Французский" v-model="nativeLanguage" /> Французский
    </label>

    <div v-if="nativeLanguage === 'Русский'">
      <p>Ваш родной язык — это русский.</p>
    </div>
    <div v-if="nativeLanguage === 'Английский'">
      <p>Your native language is English.</p>
    </div>
    <div v-if="nativeLanguage === 'Испанский'">
      <p>Su lengua materna es el español.</p>
    </div>
    <div v-if="nativeLanguage === 'Французский'">
      <p>Votre langue maternelle est le français.</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nativeLanguage: "" // Переменная для хранения выбранного родного языка
    };
  }
};
</script>
