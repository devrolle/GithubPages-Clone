<template>
    <section
        class="relative flex flex-col items-center pt-10 bg-[#222] text-white"
    >
        <button
            class="absolute top-6 right-6 bg-[#333] text-[#bbb] py-[5px] px-[10px] rounded-[4px] font-bold font-roboto text-xs"
        >
            Pages Help
        </button>
        <img src="https://pages.github.com/images/logo.svg" alt="logo" />
        <h1 class="font-roboto font-light text-5xl mt-[50px]">
            Websites for you and your projects.
        </h1>
        <h2
            class="font-roboto font-light text-lg text-[#a7a7a7] mt-[10px] mb-[60px]"
        >
            Hosted directly from your
            <a class="text-white underline" href="https://github.com"
                >GitHub repository</a
            >. Just edit, push, and your changes are live.
        </h2>
        <Slideshow :slides="slides" />
    </section>
</template>

<script lang="js">
import Slideshow from './Slideshow.vue';

const slides = [
	{src: 'https://pages.github.com/images/slideshow/bootstrap.png', alt: "bootstrap-slide", id: 0},
	{src: 'https://pages.github.com/images/slideshow/yeoman.png', alt: "yeoman-slide", id: 1},
	{src: 'https://pages.github.com/images/slideshow/facebookdesign.png', alt: "facebookdesign-slide", id: 2},
	{src: 'https://pages.github.com/images/slideshow/foundation.png', alt: "foundation-slide", id: 3},
	{src: 'https://pages.github.com/images/slideshow/ghtraining.png', alt: "ghtraining-slide", id: 4},
	{src: 'https://pages.github.com/images/slideshow/adobeos.png', alt: "adobeos-slide", id: 5},
	{src: 'https://pages.github.com/images/slideshow/jekyllrb.png', alt: "jekyllrb-slide", id: 6},
	{src: 'https://pages.github.com/images/slideshow/electron.png', alt: "electron-slide", id: 7},
	{src: 'https://pages.github.com/images/slideshow/semanticui.png', alt: "semanticui-slide", id: 8},
	{src: 'https://pages.github.com/images/slideshow/microsoft.png', alt: "microsoft-slide", id: 9},
]

export default {
	name: 'Hero',
	data() {
		return {
			slides,
		}
	},
	components: {
		Slideshow
	}
}
</script>
