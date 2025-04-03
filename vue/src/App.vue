<script>
export default {
  data() {
	return {
		arr: [1, 2, 3, 4, 5],
	}
}
};



</script>

<template>
  <ul>
		<template v-for="elem in arr">
			<li v-if="elem % 2 === 0">
				{{ elem }}
			</li>
		</template>
	</ul>
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
