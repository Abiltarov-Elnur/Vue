<template>
  <div>
    <p :class="styles">text</p>
    <button @click="setDone">Зачеркнуть</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      styles: {
        done: false,
      },
    };
  },
  methods: {
    setDone() {
      this.styles.done = true;
    },
  },
};
</script>

<style scoped>
p {
  color: red;
}

/* Класс done перечеркивает текст */
p.done {
  text-decoration: line-through;
}
</style>
