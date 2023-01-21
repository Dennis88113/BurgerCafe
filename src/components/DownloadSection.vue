<template>
<div class="download__section__container">
  <div class="download__section__title">
    <h2>Download Our Menu</h2>
  </div>
  <div class="btn">
    <my-button> Download </my-button>
  </div>
</div>
</template>

<script>
import MyButton from "@/components/UI/MyButton";

export default {

    name: "DownloadSection",

    components: {
      MyButton,
    },
}
</script>

<style scoped>
.download__section__container{
  display: flex;
  align-items: center;
  justify-content: space-around;
  height: 170px;
  width: 100%;
  background: #312F30;
  color: #FFFFFF;
}

h2{
  font-weight: 500;
  font-size: 40px;
  line-height: 47px;
}
</style>