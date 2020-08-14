<template>
   <ul class="main-footer__telephones-list">
      <li class="telephones-list__item"
         v-for="item in teleptonesList"
         :key="item"
      >
         {{item}}
      </li>
   </ul>
</template>

<script>
   export default {
      data() {
         return{
            teleptonesList: [
               "(095) 222 22 22",
               "(068) 222 22 22",
               "(063) 222 22 22"
            ]
         }
      }
      
   }
</script>

<style lang="scss">
   .main-footer__telephones-list{
      border: 2px solid #fff;
      border-top: none;
      border-bottom: none;
      padding: 0 130px;
   }
  

</style>