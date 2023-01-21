<template>
  <div class="app">
    <main-page/>
    <card-section></card-section>
    <burger-king></burger-king>
    <stock-card-section/>
    <quote-section/>
    <download-section/>
    <commercial-block/>
   </div>
</template>

<script>
import MainPage from "@/components/MainPage";
import CardSection from "@/components/CardSection";
import BurgerKing from "@/components/BurgerKing";
import StockCardSection from "@/components/StockCardSection";
import QuoteSection from "@/components/QuoteSection";
import DownloadSection from "@/components/DownloadSection";
import CommercialBlock from "@/components/CommercialBlock";


export default {
  components: {
    MainPage,
    CardSection,
    BurgerKing,
    StockCardSection,
    QuoteSection,
    DownloadSection,
    CommercialBlock,
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
*{
  margin: 0;
  padding: 0;
  font-family: 'Roboto', sans-serif
}
.app{
  height: 100%;
  min-width: 1425px;
  max-width: 1600px;
  margin: 0 auto;
}

</style>