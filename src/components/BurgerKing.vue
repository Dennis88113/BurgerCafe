<template>
<section class="burgerking__section__container">
  <div class="burgerking__section__image" v-for="picture in BurgerKingImage" :key="picture.id">
    <img :src="picture.image" :alt="picture.alt"/>
  </div>
 <card-content :DataForContentBlock="DataForContentBlock"> </card-content>

</section>
</template>

<script>
import CardContent from "@/components/UI/CardContent";

export default {
  name: "BurgerKing",

  components: {
    CardContent,
  },
  data() {
    return {
     BurgerKingImage:[
        {id:1, image: require('./../assets/BurgerKing.png'), alt: 'Burger King'},
     ],
      DataForContentBlock:[
        {id:1, title:'Burger King', description:'Together with McDonald’s, Burger King has grown to become synonymous with burgers in the US.', oldPrice:'$8', newPrice:'$6'},
       ],
    }
  }
}
</script>

<style scoped>
.burgerking__section__container{
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  height: 543px;
  background: #312F30;
  color: #FFFFFF;
}

</style>