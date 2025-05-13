<template>
  <div>
    <p :class="{active: isActive, error: hasError}">
		text
	</p>
  </div>
</template>

<script>
export default {
  data() {
	return {
		isActive: true,
		hasError: true,
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
