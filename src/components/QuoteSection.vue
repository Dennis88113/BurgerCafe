<template>
<div class="quote__section__container" >
  <quote-photo-block :Photos="Photos"> </quote-photo-block>
  <quote-block/>

</div>
</template>

<script>
import QuotePhotoBlock from "@/components/QuotePhotoBlock";
import QuoteBlock from "@/components/QuoteBlock";

export default {
  components: {
    QuotePhotoBlock,
    QuoteBlock,
  },
  data() {
    return {
      Photos: [
        {people: '1', photo: require('./../assets/Ellipse_5.png'), alt: 'girl', size: '105'},
        {people: '2', photo: require('./../assets/men_1.png'), alt: 'boy',  size: '75'},
        {people: '3', photo: require('./../assets/woman_2.png'), alt: 'girl', size: '60'},
        {people: '4', photo: require('./../assets/men_3.png'), alt: 'boy', size: '70'},
        {people: '5', photo: require('./../assets/woman_4.png'), alt: 'girl', size: '65'},
      ]
    }
  }

}

</script>

<style scoped>
.quote__section__container{
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  width:100%;
  height: 555px;
  color: #FFFFFF;
  background-color: #1C1C1C;
}

</style>