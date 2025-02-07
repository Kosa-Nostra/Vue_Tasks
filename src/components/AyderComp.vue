<template>
  
  <p :class="obj">test</p>
</template>
<script>
export default{
  data() {
	return {
		obj: {
			done: true,
			selected:  false,
		},
	}
}
}
</script>
<style> p{color: greenyellow;}</style>
