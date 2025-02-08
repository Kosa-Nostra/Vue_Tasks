<div id="app">
  <button @click="emitEvent">Нажми, чтобы испустить событие</button>
  <p>{{ message }}</p>
</div>
<script>
  new Vue({
    el: '#app',
    data: {
      message: ''
    },
    methods: {
      emitEvent() {
        // Испускаем событие (в данном случае просто обновляем данные)
        this.message = 'Это событие было испущено';
      }
    }
  });
</script>
