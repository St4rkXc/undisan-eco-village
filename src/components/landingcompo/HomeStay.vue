<script setup>
import { defineProps } from 'vue'


defineProps({
	img: {
		type: String,
		required: true,
	},
	title: {
		type: String,
		required: true,
	},
	price: {
		type: String,
		required: true,
	},
})
</script>

<template>
	<img :src="img" alt="" class="w-full h-[300px] object-cover rounded-3xl" />
	<div class="mt-4 -space-y-1">
		<p class="text-text text-xl font-semibold">{{ title }}</p>
		<p class="text-text/80 text-lg font-semibold">{{ price }}</p>
	</div>
</template>
