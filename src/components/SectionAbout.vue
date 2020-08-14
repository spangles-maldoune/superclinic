<template>
   <div class="section-about">
      <div class="container">
         <div class="section-about__layer-mask">
            <div class="section-about__description">
               <h2 class="section-about__description-title bold txt-uppercase">{{currentObj.name}}</h2>
               <p class="section-about__description-text text-margin">{{currentObj.text}}</p>
               <p class="section-about__description-text text-margin">{{currentObj.subText}}</p>
               <button class="section-about__description-button btn-outline">Деталі</button>
            </div>
            <div class="section-about__image">
               <img class="section-about__image-brain" :src=currentObj.image :alt=currentObj.id>
            </div>
            <span class="section-about__layer-mask_triangle" :style="{left: currentObj.left}">▼</span>
         </div>
      </div>
   </div>
</template>

<script>
   export default {
      props: ['currentObj'],
      data () {
         return {

            
         }
      },
      methods: {
         
      }
   }
   
  
</script>

<style lang="scss">
   .section-about{

      &__layer-mask{
         display: flex;
         justify-content: space-around;
         align-items: center;
         padding: 50px 138px 47px 119px;
         background: #F6F6F6;
         box-shadow: inset 0px 4px 10px rgba(0, 0, 0, 0.25);
         position: relative;

         &_triangle{       
            position: absolute;
            left: 360px;
            top: -13px;
            color: #E5E5E5;
            text-shadow: 0 6px 10px rgba(0, 0, 0, 0.25);
            font-size: 57px;
         }
      }

      &__description{
         margin: 0 291px 0 0;

         &-title{
            font-size: 18px;
            line-height: 22px;
            color: #000;
            margin: 0 0 34px;
         }

         &-text{
            font-size: 14px;
            line-height: 14px;
            color: #000;
            font-family: "HelveticaNeueCyr";
         }

         &-button{
            font-size: 14px;
            line-height: 17px;
            color: #2F80ED;
            padding: 14px 85px;;

         }
      }
   }

   .text-margin{
      margin: 0 0 20px 0;
   }

</style>