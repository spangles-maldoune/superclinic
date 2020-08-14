<template>
<div class="main-footer">
   <div class="main-footer__address">м. Київ, вул. Еленівська, 8</div>
   <div class="main-footer__telephones">
      <app-telephones-list></app-telephones-list>
   </div>
   <div class="main-footer__e-mail">info@clinic.com</div>
</div>
   
</template>

<script>
import TelephonesList from "./general/TelephonesList";
   export default {
      data() {
         return{

         }
      },
      components: {
         appTelephonesList: TelephonesList
      }  
   }
</script>

<style lang="scss">
   .main-footer{
      min-height: 72px;
      background: #2F80ED;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      display: flex;
      justify-content: space-around;
      align-items: center;
      color: #fff;
      font-family: "Karla", sans-serif;

      &__address{
         margin: 0 0 0 70px;
      }

      &__e-mail{
         margin: 0 140px 0 0;
      }
   }

</style>