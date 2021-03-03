<template>
  <div class="navbar">
      <div class="logo">
          <img src="/svg/Brand Builder (Color).svg" alt="logo" srcset="">
      </div>
      <div class="navitems">
        <ul>
            <li v-for="nav in navs" :key="nav.name" v-link="{path : 'your-link', activeClass: 'active', exact: true}" v-bind:class="{active:currentNav===nav}" v-on:click="currentNav = nav"><nuxt-link :to="`/${nav.link}`">{{nav.name}}</nuxt-link></li>
        </ul>
      </div>
  </div>
</template>

<script>
export default {
data(){
    return{
        currentNav:"Home",
        navs:[
            {
                name:"Home",
                link:""
            },
            {
                name:"About",
                link:"about"
            },
            {
                name:"Services",
                link:"services"
            },
            {
                name:"Portfolio",
                link:"portfolio"
            },
            {
                name:"Contact",
                link:"contact"
            },
            {
                name:"Blog",
                link:"blog"
            },
        ]
    }
},
computed: {
  currentNav: function() {
  return this.currentNav;
  }
},
};
</script>

<style lang="scss" scoped>
.nuxt-link-active{
    border-top: 5px solid $secondary-color;
}
a{
    text-decoration: none;
    color: $nav-color;
    padding-top: 33px;
}
/* .logo{
    background-color: white;
    padding: 31px 27px 52px;
    border-radius: 0 0 76px 76px;
}
.logo img{
    max-height: 86px;
    width: auto;
} */
.navbar{
    display: flex;
    justify-content: space-around;
    align-items: center;
}
ul li{
    font-size: 18px;
    list-style-type: none;
    font-weight: normal;
}
.navitems ul{
    height: 100%;
    font-size: 20px;
    font-weight: 600;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    min-width: 500px;
}
</style>