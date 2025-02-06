<script>
import { hover } from '@testing-library/user-event/dist/hover';

	export default {
        data() {
	return {
		obj: {x: 1, y: 2, z: 3},
	}
},
    methods: {
	show: function() {
		alert(new Date());
	}
}
	}
</script>
<template>
	<button @mouseover ="show">text</button>
</template>