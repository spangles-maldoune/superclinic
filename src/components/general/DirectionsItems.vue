<template>
   <ul class="section-direction__list">
      <li class="section-direction__list-item"
          v-for="item in directionItems"
          :key="item.id"
          @click="onClick(item.id)">
         <img class="section-direction__list-item_img" :src="item.imgSrc">
         <span class="section-direction__list-item_text txt-uppercase"
 
         >{{item.name}}</span>
      </li>
   </ul>
</template>

<script>
   export default {
      data() {
         return{
            directionItems:[
               {
                  id: "brain",
                  name: "Неврологія",
                  imgSrc: "./img/brain.png"
               },
               {
                  id: "healthcare",
                  name: "Масаж",
                  imgSrc: "./img/healthcare-and-medical.png"
               },
               {
                  id: "joint",
                  name: "Ревматологія",
                  imgSrc: "./img/joint.png"
               }
            ]
         }
      },
      methods:{
         onClick (id) {
            this.$emit('sendId', id);
         }

      }
   }
</script>

<style lang="scss">
   .section-direction__list{
      display: flex;
      justify-content: center;
      align-items: flex-end;

      &-item{
         display: flex;
         flex-direction: column;
         align-items: center;
         padding: 0 118px;
         cursor: pointer;

         &_img{
            display: block;
            margin: 0 0 35px;
         }
         
         &_text{
            font-size: 16px;
            line-height: 19px;
            color: #000;
            
            &:hover{
               color: #2F80ED;
            }
         }
      }

      &-item:nth-child(2){
         border: 1px solid #2F80ED;
         border-top: none;
         border-bottom: none;
         padding: 0 105px;
      }
   }
</style>