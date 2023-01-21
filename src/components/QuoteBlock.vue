<template>
  <div class="quotes__container">
    <div class="commas">
    <img src="@/assets/Vector.png" alt="commas">
    <img src="@/assets/Vector.png" alt="commas">
    </div>
    <p>Thanks a lot for the prompt service. Really appreciate. Excellence taste in Every Bite.Add a joy of best Taste. Foodie Moments.</p>
    <div class="author">
      <h2>Adele A. McNeill</h2>
      <h4>AMIRICAN</h4>
    </div>

  </div>
</template>

<script>
export default {

  name: "QuoteBlock"
}
</script>

<style scoped>
.quotes__container{
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
  justify-content: space-evenly;
  align-items: center;
  width:370px;
  height: 340px;
}
 .commas{
   display: flex;
   align-items: flex-end;
   justify-content: center;
   width: 100%;
   height: 50px;
   background-image: url('@/assets/Ellipse_15.png');
   background-size: 13%;
   background-repeat: no-repeat;
   background-position: 55%, 5px;
 }
 p, .author{
   text-align: center;
 }
 p {
   font-weight: 400;
   font-size: 16px;
   line-height: 19px;
   opacity: 0.7;
 }
.author h2{
  font-size: 24px;
  line-height: 28px;
}
.author h4{
  font-weight: 500;
  font-size: 12px;
  line-height: 14px;
  opacity: 0.7;
}
</style>