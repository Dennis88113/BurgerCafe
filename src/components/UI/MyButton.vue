<template>
  <button class="button btn">
    <slot></slot>
  </button>
</template>

<script>

export default {
}
</script>

<style scoped>
.button{
  cursor: pointer;
  text-transform: uppercase;
  color: #FFFFFF;
  font-weight: 500;
  font-size: 16px;
  line-height: 19px;
  width: 165px;
  height: 49px;
  background: #F6762C;
  border-radius: 5px;
  border: none;
  transition:.2s all linear;
}
.button:hover{
  transition:.2s all linear;
  scale: 1.1;
  font-weight:700;
  background: rgba(251, 128, 77, 0.93);
}

</style>