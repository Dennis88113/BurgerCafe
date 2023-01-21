<template>
  <div class="card__content-block" v-for="blockData in DataForContentBlock" :key="blockData.id">
    <div class= "card__content-block__title">
      <h1>{{ blockData.title }}</h1>
    </div>
    <div class= "card__content-block__description">
      <h3>{{ blockData.description }}</h3>
    </div>
    <div class="card__content-block__price">
      <span class="new-price">{{ blockData.newPrice }}</span>
      <span class="old-price">{{ blockData.oldPrice }}</span>
    </div>
    <my-button> order </my-button>

  </div>
</template>

<script>
import MyButton from "@/components/UI/MyButton";

export default {
  components: {
    MyButton,
  },
  props: {
    DataForContentBlock: {
      type: Array,
      required: true,
    },
  },

}
</script>

<style>

.card__content-block{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-evenly;
  height: 50%;
  width: 368px;
}
.card__content-block__title h1{
  font-weight: 500;
  font-size: 44px;
  line-height: 52px;
}
.card__content-block__description h3{
  font-weight: 400;
  font-size: 16px;
  line-height: 19px;
  opacity: 0.7;
}
.new-price{
  padding-right: 6px;
  font-weight: 500;
  font-size: 20px;
  line-height: 23px;
  letter-spacing: 0.1em;
  color: #F6762C;
}
.old-price{
  font-weight: 500;
  font-size: 16px;
  line-height: 19px;
  letter-spacing: 0.1em;
  text-decoration-line: line-through;
  color: #F6762C;
  opacity: 0.5;
}
</style>