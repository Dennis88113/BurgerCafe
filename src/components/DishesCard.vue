<template>
<section class="card__container" >
    <div class="dish__card" v-for="DishInf in DishCardsInf" :key="DishInf.card">
      <div class="dish__card__image">
        <img :src="DishInf.image" :alt="DishInf.dishName"/>
      </div>
      <div class="dish__card__content">
      <div class="dish__card__title" >
      {{DishInf.dishName}}
        </div>
      <div class="dish__card__description" >
        {{DishInf.dishDescription}}
      </div>
      </div>
    </div>

</section>


</template>

<script>

export default {
  props: {
    DishCardsInf: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style>
.card__container{
  color: white;
  display: flex;
  gap: 32px;
  justify-content: center;
  align-items: center;
  background-color: #1C1C1C;
  width: 100%;
  height: 550px;
}
.dish__card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  width: 262px;
  min-height: 323px;
  background: #312F30;
  border-radius: 10px;
  transition: .3s all linear;

}
.dish__card:hover {
  transition: .3s all linear;
  scale: 1.2;
}
.dish__card__image{
  height: 162px;
}
.dish__card__content{
display: flex;
align-items: center;
flex-direction: column;
justify-content: space-evenly;
height: 161px;
}
.dish__card__title{
  font-weight: 500;
  font-size: 20px;
  line-height: 23px;
}
.dish__card__description{
  width: 80%;
  text-align: center;
  font-weight: 400;
  font-size: 16px;
  line-height: 19px;
  opacity: 0.7;
}
</style>