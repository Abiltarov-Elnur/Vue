<template>
	<User
		v-for="user in users"
		:name="user.name"
		:surn="user.surn"
		:key="user.id"
	/>
</template>

<script>
	export default {
		props: ['name', 'surn'],
		data() {
	return {
		users: [
			{
				id: 1,
				name: 'name1',
				surn: 'surn1'
			},
			{
				id: 2,
				name: 'name2',
				surn: 'surn2'
			},
			{
				id: 3,
				name: 'name3',
				surn: 'surn3'
			},
		],
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
