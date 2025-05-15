<template>
	<User name="john" surn="smit" />
  {{ name }}
	{{ surn }}
</template>

<script>
	export default {
		props: ['name', 'surn'],
		data() {
			return {
				
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
