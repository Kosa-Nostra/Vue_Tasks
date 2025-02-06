<script>
import { hover } from '@testing-library/user-event/dist/hover';

	export default {
        data() {
	return {
		num1: 1,
		num2: 2,
	}
},
    methods: {
	show: function() {
		alert((this.num1)+(this.num2));
	}
}
	}
</script>
<template>
	<button @click ="show">text</button>
</template>