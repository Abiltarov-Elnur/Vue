<template>
  <button @click="$emit('hello')">Сказать привет</button>
</template>

<script>
export default {
  emits: ['hello'],
};
</script>
