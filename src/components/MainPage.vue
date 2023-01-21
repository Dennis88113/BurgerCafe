<template>
  <section class="main-page">
  <nav-menu :menuItems="menuItems"/>
  <content-block :contentBlock="contentBlock"></content-block>
  </section>
</template>

<script>
// import MyLogo from "@/components/MyLogo";
import NavMenu from "@/components/NavMenu";
import ContentBlock from "@/components/ContentBlock";

export default {
  components: {
    NavMenu,
    ContentBlock,

  },

  data() {
    return {
      menuItems:[
        {id:1, content:'home'},
        {id:2, content:'pages'},
        {id:3, content:'our offer'},
        {id:4, content:'pricing'},
        {id:5, content:'shop'},
      ],
    }
  }
}
</script>

<style scoped>
.main-page{
display: flex;
flex-direction: column;
background-image: url("./../assets/main-bgr.png");
background-repeat: no-repeat;
background-size: 100%,100%;
min-width: 1425px;
max-width: 1600px;
height: 100%;
min-height:788px;

}
</style>