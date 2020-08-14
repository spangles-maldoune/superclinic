<template>
	<div class="wrapper">
		<app-section-main></app-section-main>
		<app-section-direction @sendId="getId"></app-section-direction>
		<app-section-about :currentObj="stateObj[id]"></app-section-about>
	</div>
</template>

<script>
	import SectionMain from './components/SectionMain';
	import SectionDirection from "./components/SectionDirection";
	import SectionAbout from "./components/SectionAbout"

	export default {
		data () {
			return {
				stateObj: {
					brain: {
						name: "неврологія",
						text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
						subText: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
						image: "./img/image_brain.png",
						left: "360px"
					},
					healthcare: {
						name: "Масаж",
						text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
						subText: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
						image: "./img/image_healthcare-and-medical.png",
						left: "682px"
					},
					joint: {
						name: "ревматологія",
						text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
						subText: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
						image: "./img/image_joint.png",
						left: "1012px"
					}
				},
				id: "brain"
			}
		},
		methods: {
			getId(id) {
				this.id = id;
			}
		},
		components: {
			appSectionMain: SectionMain,
			appSectionDirection: SectionDirection,
			appSectionAbout: SectionAbout
		}
	}
</script>

<style lang="scss">
	@import url('./assets/css/reset.css');
	@import url('./assets/css/fonts.css');
	@import url('./assets/css/global-styles.css');
	@import url('./assets/css/media_queries.css');
</style>
