<template>
	<div class="main-header" :class="{'header-fixed': isActive}">
		<div class="container">
			<header class="main-header__menu">
				<div class="main-header__menu_logo">
					<img class="main-header__menu_logo-img" src="../../public/img/logo.png" alt="logo">
				</div>
				<app-burger-menu></app-burger-menu>
				<app-menu-list></app-menu-list>
				<button class="main-header__button bold btn-outline txt-uppercase">Записатись на прийом</button>
			</header>
		</div>
	</div>
</template>

<script>
	import MenuList from './general/MenuList';
	import BurgerMenu from './general/BurgerMenu';
	export default {
		data () {
			return {
				isActive: false,
				name: 'Header'
			}
		},
		components: {
			appMenuList: MenuList,
			appBurgerMenu: BurgerMenu
		},
		created () {
    		window.addEventListener('scroll', this.handleScroll);
  		},
  		destroyed () {
    		window.removeEventListener('scroll', this.handleScroll);
  		},
		methods:{
			handleScroll (event) {
				const pageYOffset = event.target.defaultView.pageYOffset;
				const innerWidth = event.target.defaultView.innerWidth;
				if(pageYOffset > 200 && innerWidth > 1149) {
					this.isActive = true;
				} else {
					this.isActive = false;
				}
			}
		}
	}
</script>

<style lang="scss">
	.main-header{
		background: rgba(255, 255, 255, 0.9);
		box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
		margin: 0 0 64px;
		top: -72px;

		&__menu{
			width: 100%;
			height: 72px;
			display: flex;
			justify-content: space-between;
			align-items: center;

			&_logo{
				margin: 0 0 0 206px;
			}
		}

		&__button{
			padding: 7px 12px;
			color: #2F80ED;
			font-size: 14px;
			line-height: 17px;
			margin: 0 135px 0 0;
		}
	}

	.container{
		max-width: 1440px;
		margin: 0 auto;
	}

	.header-fixed{
		position: fixed;
		width: 100%;
		top: 0;
		z-index: 10;
		transition: top 1s;
	}

</style>
