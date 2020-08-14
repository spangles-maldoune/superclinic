<template>
   <section class="burger-menu">
      <div class="burger-menu__wrap"
           @click="toggleMenu">
         <span class="burger-menu__wrap-button"></span>
      </div>
      <div class="burger-menu__main" :class="{'burger-menu__active': isToggle}">
         <ul class="burger-menu__main-list">
            <li class="burger-menu__main-list_item"
                v-for="item in menuItems"
                :key="item"
            >
               <a class="burger-menu__main-list_item-link bold txt-uppercase" href="#">{{item}}</a>
            </li>
         </ul>
         <button class="burger-menu__main-button bold btn-outline txt-uppercase">Записатись на прийом</button>
      </div>
   </section>

   
</template>

<script>
   export default {
      data() {
         return {
            menuItems: [
               "Переваги",
               "ціни",
               "лікування",
               "Контакти"
            ],
            isToggle: false
         }
      },
      methods:{
         toggleMenu() {
            if(!this.isToggle) {
               this.isToggle = true;
            } else {
               this.isToggle = false;
            }
            
         }
      }
      
   }
</script>

<style lang="scss">
   .burger-menu{
      position: absolute;
      display: none;

      &__wrap{
         cursor: pointer;
         position: relative;
         width: 40px;
         height: 32px;
         top: 0;

         &-button, &-button:before, &-button:after{
            width: 40px;
            height: 4px;
            background: #2F80ED;
            top: 13px;
            position: absolute;
         }

         &-button:before, &-button:after{
            content: '';
            width: 40px;
            height: 4px;
            background: #2F80ED;
            top: 13px;
            position: absolute;
         }

         &-button:before{
            top: -13px;
	         left: 0;
         }
      }

      &__main{
         position: absolute;
         top: 51px;
         left: -20px;
         width: 190px;
         height: 100vh;
         background: #fff;
         box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
         display: none;

         &-list{
            margin: 0 0 40px;

            &_item{
               margin: 10px 0 15px 15px;

               &-link{
                  font-size: 14px;
                  line-height: 17px;
                  color: #2F80ED;
               }
            }
         }

         &-button{
            padding: 7px 12px;
            color: #2F80ED;
            font-size: 12px;
            line-height: 17px;
            margin: 0 10px;
         }
      }

      &__active{
         display: block;
      }
   }


</style>