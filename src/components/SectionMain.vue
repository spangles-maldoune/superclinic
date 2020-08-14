<template>
	<div class="section-main">
		<div class="section-main__layer-mask">
			<app-main-header></app-main-header>
			<app-main-about></app-main-about>
			<app-main-footer></app-main-footer>
		</div>
	</div>
</template>

<script>
	import MainHeader from './MainHeader';
	import MainAbout from "./MainAbout";
	import MainFooter from "./MainFooter";

	export default {
		data () {
			return {

			}
		},
		methods: {

		},
		components: {
			appMainHeader: MainHeader,
			appMainAbout: MainAbout,
			appMainFooter: MainFooter
		}
	}
</script>

<style lang="scss">
	@import url('../assets/css/reset.css');
	@import url('../assets/css/fonts.css');
	@import url('../assets/css/global-styles.css');

	.section-main{
		background: url('../../public/img/Mask Group.jpg') no-repeat center/cover;
		width: 100%;
		min-height: 618px;
		
		&__layer-mask{
			min-height: 618px;
			background: linear-gradient(87.68deg, rgba(255, 255, 255, 0) 18.73%, rgba(255, 255, 255, 0.9) 78.76%);
		}
	}
</style>
