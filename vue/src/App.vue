<script>
export default {
  data() {
	return {
		text: 'abvs'
	}
  },
  methods: {
    show: function() {
		let text = this.cape(this.text);
		alert(text);
	},
	cape: function(str) {
		return str[0].toUpperCase() + str.slice(1);
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
