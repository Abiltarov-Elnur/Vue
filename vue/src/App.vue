<script>
export default {
  data() {
	return {
		users: [
			{
				name: 'name1',
				surn: 'surn1',
			},
			{
				name: 'name2',
				surn: 'surn2',
			},
			{
				name: 'name3',
				surn: 'surn3',
			},
		]
	}
}
};



</script>

<template>
  <p v-for="user in users">
		{{ user.name }}
		{{ user.surn }}
	</p>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
