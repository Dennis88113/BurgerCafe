<template>
  <div class="stock-card">
  <div class="card__content-block card"
       v-for="StockBlockData in DataForStockBlock"
       :key="StockBlockData.card"
       :class="StockBlockData.card=='1'||StockBlockData.card=='3'? 'alignEnd': 'alignStart'"
       :style="{backgroundImage: StockBlockData.backgroundImage}">
    <div class=content>

             <div class= "card__content-block__title title">
      <h1>{{ StockBlockData.title }}</h1>
    </div>
    <div class= "card__content-block__description">
      <h3>{{ StockBlockData.description }}</h3>
    </div>
    <div class="card__content-block__price">
      <span class="new-price price">{{StockBlockData.newPrice }}</span>
      <span class="old-price price">{{StockBlockData.oldPrice }}</span>
    </div>
    <div class="btn">
    <my-button> order </my-button>
    </div>
  </div>
  </div>
  </div>
</template>

<script>
import MyButton from "@/components/UI/MyButton";

export default {
  components: {
    MyButton,
  },

  data() {
    return {
      DataForStockBlock: [
        {
          card: 1,
          title: 'Dairy Queen',
          description: 'Dairy Queen is one of the biggest fast-food.',
          oldPrice: '$6',
          newPrice: '$4',
          backgroundImage: `url(${require('../assets/coffe.png')})`,
        },
        {
          card: 2,
          title: 'Pizza Hut',
          description: 'Although the Pizza Hut Menu Prices.',
          oldPrice: '$7',
          newPrice: '$3',
          backgroundImage: `url(${require('../assets/pizza.png')})`,
        },
        {
          card: 3,
          title: 'Burger King',
          description: 'Together with McDonald’s, Burger King.',
          oldPrice: '$6',
          newPrice: '$5',
          backgroundImage: `url(${require('../assets/burger.png')})`,
        },
        {
          card: 4,
          title: 'Papa John’s',
          description: 'Papa John’s is one of the most popular fast-food.',
          oldPrice: '$8',
          newPrice: '$6',
          backgroundImage: `url(${require('../assets/doner.png')})`,

        },
      ],
    }
},
}

</script>

<style scoped>
.btn{
  width: 141px;
  height: 39px;
  font-size: 12px;
  line-height: 14px;
}
.title{
  font-size: 30px;
  line-height: 35px;
}
.price{
  font-size: 16px;
  line-height: 19px;
}
.stock-card{
  display: flex;
  align-content: center;
  justify-content: center;
  gap: 30px;
  flex-wrap: wrap;
}
.card__content-block__description{
  width: 251px;
}

.card{
  display: flex;
  width: 555px;
  height: 300px;
  background-size: cover;
  background-repeat: no-repeat;
}
.alignEnd{
  align-items: flex-end;
  padding-right: 30px;
  justify-content: space-evenly;

}
.alignStart{
  align-items: flex-start;
  padding-left: 30px;
  justify-content: space-evenly;
}
.content{
  height: 80%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}
</style>