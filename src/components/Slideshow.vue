<template>
    <div class="max-w-[830px]">
        <Slide :slide="slide" :activeIndex="index" v-for="slide in slides" />
    </div>
</template>

<script lang="js">
import Slide from './Slide.vue';
let index = 0;

export default {
	name: 'Slideshow',
	props: {
		slides: Array,
	},
	mounted: function () {
		this.updater = setInterval(() => {
			if (this.index >= this.slides.length - 1) {
				this.index = 0
			} else {
				this.index++
			}
		}, 2500)
	},
	data() {
		return {
			index: 0,
			updater: null,
		}
	},
	components: {
		Slide,
	},
	beforeUnmount: function () {
		clearInterval(this.updater)
	}
}
</script>
