<template>
  <div>
    <h3>Какие языки вы знаете?</h3>
    <label>
      <input type="checkbox" value="Русский" v-model="languages" /> Русский
    </label>
    <label>
      <input type="checkbox" value="Английский" v-model="languages" /> Английский
    </label>
    <label>
      <input type="checkbox" value="Испанский" v-model="languages" /> Испанский
    </label>
    <label>
      <input type="checkbox" value="Французский" v-model="languages" /> Французский
    </label>

    <div v-if="languages.length > 0">
      <h4>Вы знаете следующие языки:</h4>
      <ul>
        <li v-for="language in languages" :key="language">{{ language }}</li>
      </ul>
    </div>
    <div v-else>
      <p>Вы не выбрали языки.</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      languages: [] // Массив для хранения выбранных языков
    };
  }
};
</script>
