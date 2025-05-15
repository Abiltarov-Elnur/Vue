<template>
	<User :name="name" :surn="surn" />
</template>

<script>
	export default {
		
		data() {
	return {
		name: 'john',
		surn: 'smit',
	}
}
	}
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
