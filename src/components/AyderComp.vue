<template>
  <div>
    <div v-for="(item, index) in items" :key="index">
      <p v-if="item.visible">{{ item.text }}</p>
      <button @click="toggleVisibility(index)">
        {{ item.visible ? 'Скрыть' : 'Показать' }} абзац {{ index + 1 }}
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { text: 'Текст первого абзаца', visible: false },
        { text: 'Текст второго абзаца', visible: false },
        { text: 'Текст третьего абзаца', visible: false }
      ]
    };
  },
  methods: {
    toggleVisibility(index) {
      this.items[index].visible = !this.items[index].visible;
    }
  }
};
</script>
