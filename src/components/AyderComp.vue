<script>
	export default {
        data() {
	return {
		name: 'john',
		surn: 'smit',
        attr: 'img.png',
        text: 'page',
		href: 'page.html',
	}
}	
	}
</script>
<template>
	<div>
        <p>{{ name }}</p>
        <p>{{ surn }}</p>
        <a :href="page.html">page</a>
	</div>
</template>
