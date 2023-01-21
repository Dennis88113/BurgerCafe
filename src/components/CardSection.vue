<template>
    <dishes-card :DishCardsInf="DishCardsInf"></dishes-card>

</template>

<script>
import DishesCard from "@/components/DishesCard";

export default {
  data() {
    return {
      DishCardsInf:[
        {card:1, dishName:'Chicken Paella', image: require('./../assets/Rectangle32.png'), dishDescription:'We just don\'t make and sell food.Good food warms.'},
        {card:2, dishName:'Taco Del Mar', image: require('./../assets/Rectangle33.png'), dishDescription:'Taco Del Mar brings the best out of Mexican cuisine with fresh.'},
        {card:3, dishName:'Bon Au Pain', image: require('./../assets/Rectangle34.png'), dishDescription:'Bon Au Pain is a pioneer in the healthy fast food scene.'},
        {card:4, dishName:'Pizza Hut.', image: require('./../assets/Rectangle35.png'), dishDescription:'Although the Pizza Hut Menu Prices have tumbled over the years.'},
      ]
    }
  },
 components:{
  DishesCard
},

}
</script>

<style scoped>

</style>