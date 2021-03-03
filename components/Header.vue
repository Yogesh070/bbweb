<template>
  <div class="header">
    <div>
      <img src="/svg/Email.svg" alt="">
      <i>mail@brandbuilder.com.np </i>
      <img src="/svg/Phone.svg" alt="">
      <i> 98506636365</i>
    </div>
      
      <div class="socials">
        <ul>
          <li v-for="social in socials" :key="social.name">
          <a :href="social.link" target="_blank">
            <img :src="`/svg/${social.icon}`" :alt="social.name">
          </a>
        </li>
        </ul>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      socials:[
            {
                icon:"fb.svg",
                name:"facebook",
                link:"http://www.facebook.com"
            },
            {
                icon:"Instagram.svg",
                name:"instagram",
                link:"http://www.instagram.com"
            },
            {
                icon:"twitter-1.svg",
                name:"twitter",
                link:"http://www.twitter.com"
            },
        ],
    }
  },

}
</script>

<style lang="scss"scoped>
.header{
    padding: 15px 0;
    border-bottom: 1px solid black;
    display: grid;
    grid-template-columns: 1fr 1fr;
    justify-items: center;
}
.socials{ 
  ul{
    display: flex;
    li{
      padding: 0 10px;
    }
  }
  img{
    height: 20px;
    width: 20px;
  }
}
</style>