<template>
  <div class="content-container">
<div class="content-block">
  <h3 class="subtitle">{{contentBlock[1].subtitle}}</h3>
  <h1 class="title">{{contentBlock[0].title}}</h1>
  <p class="content">{{contentBlock[2].content}}</p>
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
  data() {
    return {
      contentBlock: [
        { id:1, title: 'The fastest food, for instant hunger.'},
        { id:2, subtitle: 'FAST FOOD BURGERS'},
        { id:3, content: 'Some food has looked so awful that it\'s looked like something that the dog\'s brought home, yet after one mouthful I\'ve been left eating my thoughts, my words & my food and gone back for seconds.'},
      ],
    }
  }
}
</script>

<style scoped>
:is(h1, h3, p, nav) {
  color: #FFFFFF;
}
.content-container{
  margin-left: 170px;
  margin-top: 125px;
  width: 41%;
  height: 100%;
}
.content-block{
  max-width: 605px;
  max-height:300px;
}

h3{
  margin-bottom: 7px;
  font-weight: 500;
  font-size: 14px;
  line-height: 16px;
  letter-spacing: 0.1em;
}
h1{
  margin-bottom: 37px;
  font-weight: 500;
  font-size: 57px;
  line-height: 67px;
}
p{
  width: 84%;
  margin-bottom: 42px;
  font-weight: 400;
  font-size: 18px;
  line-height: 21px;
  opacity: 0.7;
}

</style>