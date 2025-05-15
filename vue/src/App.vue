<template>
  <div>
    <button @click="handleFirst">Вызвать первую</button>
    <button @click="handleSecond">Вызвать вторую</button>
  </div>
</template>

<script>
export default {
  emits: ['first-action', 'second-action'],
  methods: {
    handleFirst() {
      this.$emit('first-action');
    },
    handleSecond() {
      this.$emit('second-action');
    },
  },
};
</script>
