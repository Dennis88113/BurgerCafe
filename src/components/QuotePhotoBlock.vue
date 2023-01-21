<template>
<div class="photo__block__container">
     <div class="photo__block" v-for="Picture in Photos" :key="Picture.people"
          :style ="{width: Picture.size + 'px', height: Picture.size + 'px'}"
          :class = "'person' + '-'+ Picture.people">
  <img :src="Picture.photo" :alt="Picture.alt"/>
</div>
  </div>
</template>

<script>
export default {
  props: {
    Photos: {
      type: Array,
      required: true,
    },
  },


}
</script>

<style scoped>
.photo__block__container{
  position: relative;
  display: flex;
  width:370px;
  height: 360px;
  background-image: url('@/assets/Ellipse_10.png'),url('@/assets/Ellipse_11.png');
  background-repeat: no-repeat;
  background-position: center;
}

img{
  border-radius: 50%;
  width: 100%;
  height: 100%;

}
.photo__block{
  border-radius: 50%;
  position: absolute;
}
.person-1 {
  top: 35%;
  left: 37%;
  box-shadow: 0px 0px 100px -24px rgba(246, 118, 44, 0.78);
}
.person-2 {
  top: 10%;
  left: 2%;
}

.person-3 {
  background-color: #d8dcde;
  top: 2%;
  left: 70%;
}
.person-4 {
  top: 78%;
  left: 11%;
}
.person-5 {
  top: 70%;
  left: 77%;
}
</style>