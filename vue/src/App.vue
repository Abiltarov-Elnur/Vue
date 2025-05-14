<template>
	<select v-model="selected">
		<option v-for="option in options">{{ option }}</option>
	</select>
	
	<p>{{ selected }}</p>
</template>

<script>
export default {
  data() {
	return {
		selected: 'value1',
		options: ['value1', 'value2', 'value3'],
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
