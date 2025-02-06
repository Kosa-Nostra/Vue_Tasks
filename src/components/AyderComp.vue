<script>
	export default {
        data() {
	return {
		arr: ['x', 'y', 'z'],
	}
}
	}
</script>
<template>
	<div>
        <p>{{ arr[0] }}</p>
        <p>{{ arr[1] }}</p>
        <p>{{ arr[2] }}</p>
	</div>
</template>
