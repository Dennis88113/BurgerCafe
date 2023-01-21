<template>
  <div class="stock-card-section__container">
<stock-card></stock-card>
  </div>

</template>

<script>
import StockCard from "@/components/StockCard";

export default {
  name: "StockCardSection",

  components: {
    StockCard,
  },
 }
</script>

<style scoped>
.stock-card-section__container{
  display: flex;
  color: #FFFFFF;
  height:820px;
  width: 100%;
  background-color: #1C1C1C;
}
</style>