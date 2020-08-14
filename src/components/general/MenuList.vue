<template>
   <ul class="main-header__menu-list">
      <li class="menu-list__item" 
          v-for="item in menuItems"
          :key="item">
         <a class="menu-list__item-link bold txt-uppercase" href="#">{{item}}</a>
      </li>
   </ul>
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
            ]
         }
      }
      
   }
</script>

<style lang="scss">
   .main-header__menu-list{
      display: flex;
   }

   .menu-list{
      &__item{
         margin: 0 23px 0 0;

         &-link{
            font-size: 14px;
            line-height: 17px;
            color: #2F80ED;
         }
      }

      &__item:last-child{
         margin: 0;
      }
   }

</style>