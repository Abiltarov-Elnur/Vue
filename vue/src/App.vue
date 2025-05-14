<template>
	<button v-bind:disabled="isDisabled">btn</button>
</template>

<script>
export default {
  data() {
	return {
		isDisabled: true,
	}
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
