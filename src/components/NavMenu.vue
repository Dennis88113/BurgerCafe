<template>
  <header class="navigation__container">
    <div class="navigation__logo">
      <my-logo></my-logo>
    </div>

    <div class="navigation">
      <div class="navigation__logo"></div>
      <div class="navigation__menu">
        <ul
            class="navigation__menu__items"
            v-for="item in menuItems"
            :key="item.id"
        >
          <li class="item">
            <a href="#">{{ item.content }}</a>
          </li>
        </ul>
      </div>
    </div>
    <my-button> order </my-button>
  </header>

</template>

<script>
import MyButton from "@/components/UI/MyButton";
import MyLogo from "@/components/MyLogo";


export default {
  components: {
    MyButton,
    MyLogo,
  },

  props: {
    menuItems: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.navigation__container{
  margin-top: 30px;
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.navigation__menu__items {
  list-style: none;
  display: inline-flex;
}
.item {
  margin-right: 15px;
}
.item a {
  text-transform: uppercase;
  text-decoration: none;
  color: #FFFFFF;
  opacity: 0.7;
}
.item a::active{
  transform: scale(1.03);
  opacity: 1;
}
.item a:hover {
  text-shadow: 1px 1px 5px rgba(255,  255,  255, 1);
  transform: scale(1.01);
  transition: .2s;
  opacity: 1;
}
</style>
