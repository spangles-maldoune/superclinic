<template>
   <div class="container align">
      <section class="main-about">
         <span class="main-about__label txt-uppercase">ПОВНИЙ КОМПЛЕКС МЕДИЧНИХ ПОСЛУГ</span>
         <h1 class="main-about__title">Європейські стандарти <br>медичної допомоги</h1>
         <button class="main-about__button txt-uppercase btn-outline bold">про клініку</button>
      </section>
   </div>
</template>

<script>
   export default {

   }
</script>

<style lang="scss">
.main-about{
   margin: 0 131px 90px 0;

   &__label{
      font-size: 16px;
      line-height: 19px;
      color: #2F80ED;
   }

   &__title{
      font-family: "PFDinTextCondPro";
      font-size: 50px;
      line-height: 55px;
      margin: 0 0 64px;
   }

   &__button{
      background: #2F80ED;
      color: #FFFFFF;
      font-size: 14px;
      line-height: 17px;
      padding: 8px 59px;
      margin: 0 0 233px;
   }
}

</style>