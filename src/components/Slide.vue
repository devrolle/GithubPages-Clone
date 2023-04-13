<template>
    <img
        :src="slide.src"
        :alt="slide.alt"
        v-show="id === activeIndex"
        :class="id === activeIndex && 'animate-fade-in'"
    />
</template>

<script lang="js">
export default {
	name: 'Slide',
	props: {
		slide: Object,
		activeIndex: Number,
	},
	data() {
		return {
			id: this.slide.id,
		}
	},
	watch: {
		activeIndex: function (newVal, oldVal) {

		}
	},
}
</script>
