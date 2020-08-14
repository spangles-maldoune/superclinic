<template>
   <div class="section-direction">
      <div class="container">
         <div class="section-direction__title">
				<div class="section-direction__title-label txt-uppercase">Комплексний підхід до Вашого здоров'я</div>
				<h2 class="section-direction__title-subtitle">Ключові напрямки</h2>
				<div class="section-direction__title-star">
					<img src="../../public/img/Star.png" alt="Star">
				</div>
         </div>
			<app-directions-items @sendId="getId"></app-directions-items>

      </div>
   </div>
</template>

<script>
import DirectionsItems from "./general/DirectionsItems";
   export default {
      data() {
         return{
           
         }
		},
		components: {
			appDirectionsItems: DirectionsItems
		},
		methods:{
			getId (id) {
				this.$emit('sendId', id);
			}

		}
   }
</script>

<style lang="scss">
	.section-direction{
		background: #E5E5E5;
		padding: 46px 0 81px;

		&__title{
			display: flex;
			flex-direction: column;
			align-items: center;
			margin: 0 0 50px;

			&-label{
			font-size: 14px;
			line-height: 17px;
			color: #C4C4C4;
			margin: 0 0 11px;
			}

			&-subtitle{
				font-size: 30px;
				line-height: 36px;
				color: #000;
				margin: 0 0 8px;
			}

			&-star{
				position: relative;

				&::before{
					content: '';
					position: absolute;
					width: 50px;
					height: 1px;
					background: #2F80ED;
					top: 14px;
    				left: -56px;
				}

				&::after{
					content: '';
					position: absolute;
					width: 50px;
					height: 1px;
					background: #2F80ED;
					top: 14px;
    				right: -56px;
				}
			}
		}
	}
</style>