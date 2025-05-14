<template>
	<textarea v-model="text"></textarea>
	<p>{{ text }}</p>
</template>

<script>
export default {
  data() {
	return {
		text: '',
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
