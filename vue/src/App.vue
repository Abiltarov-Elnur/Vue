<template>
	<ul>
		<li v-for="user in users" :key="user.id">
			<template v-if="!user.isEdit">
				{{ user.name }}
				{{ user.surn }}
				<button @click="edit(user)">
					edit
				</button>
			</template>
			<template v-else>
				<input v-model="user.name">
				<input v-model="user.surn">
				<button @click="save(user)">
					save
				</button>
			</template>
		</li>
	</ul>
</template>

<script>
export default {
  data() {
	return {
		users: [
			{
				id: 1,
				name: 'name1',
				surn: 'surn1',
				isEdit: false,
			},
			{
				id: 2,
				name: 'name2',
				surn: 'surn2',
				isEdit: false,
			},
			{
				id: 3,
				name: 'name3',
				surn: 'surn3',
				isEdit: false,
			},
		]
	}
},
methods: {
	edit(user) {
		user.isEdit = true;
	},
	save(user) {
		user.isEdit = false;
	},
}
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
