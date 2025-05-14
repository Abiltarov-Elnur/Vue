<template>
	<input v-model="message">
	<p>{{ message }}</p>
</template>

<script>
export default {
  data() {
	return {
		message: 'hello',
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
