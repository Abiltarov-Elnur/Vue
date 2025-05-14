<template>
	<input type="checkbox" v-model="arr" value="v1">
	<input type="checkbox" v-model="arr" value="v2">
	<input type="checkbox" v-model="arr" value="v3">
</template>

<script>
export default {
  data() {
	return {
		arr: [],
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
