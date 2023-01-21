<template>
<footer class="footer commercial__block">
    <navigation class="navigation__menu">
      <div class="commercial__block__web-info">
        <my-logo></my-logo>
        <div class="commercial__block__web__info">
          <div class="web__info">
            <div class="icon">
              <img src="./../assets/mail.png" alt="mail">>
            </div>
            <div class="e-mail">
              <a href="mailto:fastfood_usa@gmail.com" target="_blank">fastfood_usa@gmail.com</a>
            </div>
          </div>
          <div class="web__info">
            <div class="icon">
              <img src="./../assets/web.png" alt="website">>
            </div>
            <div class="e-mail">
              <a href="www.fastfood_usa.com" target="_blank"> www.fastfood_usa.com</a>
            </div>
          </div>
        </div>
      </div>
    <div class="navigation" v-for="inf in CommercialInfo" :key="inf.menuTitle">
    <h4>{{inf.menuTitle}}</h4>
    <ul class="navigation__items">
      <li><a href="#"> {{inf.menuItem1}}</a></li>
      <li><a href="#"> {{inf.menuItem2}}</a></li>
      <li><a href="#"> {{inf.menuItem3}}</a></li>
    </ul>
    </div>
    <div>
      <h4 class="social">Social Handles</h4>
      <ul class="social__media">
        <li><a href="#"> <img src="./../assets/facebook.png" alt="facebook"></a></li>
        <li><a href="#"> <img src="./../assets/twitter.png" alt="twitter"> </a></li>
        <li><a href="#"><img src="./../assets/instagram.png" alt="instagram"> </a></li>
        <li><a href="#"><img src="./../assets/linkedin.png" alt="linkedin"> </a></li>
      </ul>
    </div>
  </navigation>
</footer>
</template>

<script>
import MyLogo from "@/components/MyLogo";

export default {
  name: "CommercialBlock",

data(){
    return {
    CommercialInfo: [
        {menuTitle: 'Our menu', menuItem1: 'Breakfast', menuItem2: 'Lunce', menuItem3: 'Dinner', },
        {menuTitle: 'Information', menuItem1: 'About us ', menuItem2: 'Testimonial', menuItem3: 'Event'},
        {menuTitle: 'Useful Links', menuItem1: 'Services', menuItem2: 'Support', menuItem3: 'Conditions'},
    ]
    }
    },

  components: {
    MyLogo,
  },
}
</script>

<style scoped>
.footer {
  width: 100%;
  display: flex;
  justify-content: center;
  height: 381px;
  background-color: #1C1C1C;
}
.web__info{
  display: flex;
  margin-bottom: 5px;
}
.commercial__block__web-info{
  width: 30%;
  height: 125px;
}
.navigation__menu{
  width:70%
}
h4{
  color: #FFFFFF;
  font-weight: 500;
  font-size: 16px;
  line-height: 19px;
}

li{
  margin-bottom: 5px;
  list-style: none;
}
a{
  text-decoration: none;
  color: #FFFFFF;
  font-weight: 400;
  font-size: 12px;
  line-height: 14px;
  transition: .2s;
  opacity: 0.8;
}
a:hover {
  text-shadow: 1px 1px 5px rgba(255,  255,  255, 1);
  transform: scale(1.01);
  transition: .2s;
  opacity: 1;
}
.navigation {
  display: flex;
  height: 125px;
  gap: 20px;
  flex-direction: column;
  margin-right: 100px;
}
.navigation__menu{
  margin-top: 120px;
  display: flex;
}
.social__media{
  display: flex;
  gap: 12px;
}
.social{
  margin-bottom: 25px;
}
.logo {
  margin-bottom: 18px;
}
</style>