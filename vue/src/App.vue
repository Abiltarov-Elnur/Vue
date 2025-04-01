<script>
export default {
  data() {
	return {
		num1: 1,
		num2: 2,
	}
  },
  methods: {
	show: function() {
		alert(this.num1 + this.num2);
	}
  }

};
</script>

<template>
  {{ show() }}
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
