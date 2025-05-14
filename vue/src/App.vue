<template>
	<ul>
		<li v-for="(item, index) in items" :key="index">
			{{ item }}
			<button @click="removeItem(index)">remove</button>
		</li>
	</ul>
</template>

<script>
export default {
  data() {
    return {
      items: ['a', 'b', 'c', 'd', 'e'],
    };
  },
  methods: {
    removeItem(index) {
      this.items.splice(index, 1);
    },
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
