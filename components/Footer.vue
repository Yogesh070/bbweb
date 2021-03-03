<template>
<div class="container">
      <div class="top-bar">
        
            <img src="/svg/Brand Builder (White).svg" alt="logo" srcset="" id="logo">
        
        <div class="socials">
              <ul>
                <li v-for="social in socials" :key="social.name">
                    <a :href="social.link" target="_blank">
                        <img :src="`/svg/SVG_Organized/Social_Media/${social.icon}`" :alt="social.name">
                    </a>
                </li>
              </ul>
          </div>
      </div>
      <div class="bottom-box">
            <div class="services">
            <h2>Services</h2>
            <ul>
                <li v-for="(service,index) in services " :key="index">{{service}}</li>
            </ul>
                </div>
                <div class="contacts">
                    <h2>Contact</h2>
                    <ul>
                        <li v-for="(contact,index) in contacts" :key="index">{{contact}}</li>
                    </ul>
            </div>
            <div class="news-feeds">
                <h2>News Feeds</h2>
                <ul>
                    <li v-for="nav in navs" :key="nav.name"><nuxt-link :to="`/${nav.link}`">{{nav.name}}</nuxt-link></li>
                </ul>
            </div>
      </div>
      
      <div class="copyright">
          <div>
              <p>© 2020  All Rights Reserved</p>
          </div>
          <div class="privacy">
              <p>Privacy</p>
              <p>Terms and Condition</p>
          </div>
       </div>
  </div>
</template>

<script>
export default {
data(){
    return{
        services:["Product Stratergy","Product Engineering","Artitecture","UX/UI Desing" ,"App Development"],
        contacts:["mail@brandbuilder.com","+9805821350","Panthi galli, Chipledhunga"],
        socials:[
            {
                icon:"Fb.svg",
                name:"facebook",
                link:"http://www.facebook.com"
            },
            {
                icon:"Twitter.svg",
                name:"twitter",
                link:"http://www.twitter.com"
            },
            {
                icon:"Insta.svg",
                name:"instagram",
                link:"http://www.instagram.com"
            },
        ],
        navs:[
            {
                name:"Home",
                link:""
            },
            {
                name:"About Us",
                link:"about"
            },
        ]
    }
}
}
</script>
<style scoped>
.container{
    background-image: url("/svg/SVG_Organized/Footer Background.svg");
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    color: white;
    font-size: 14px;
}
a{
    color: white;
    cursor: pointer;
}
#logo{
    height: 100px;
}
.top-bar{
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom:1px solid white;
    padding: 10px 0;
    margin: 0 100px;
}
.socials ul{ 
    display: flex;
}
.socials ul li{
    padding: 0 10px;
}
.socials img{
    height: 50px;
    width: 30px;
}
.bottom-box{
    display: grid;
    grid-template-columns: 1fr 1fr 2fr;
    justify-items: center;
    margin: 50px 0;
}
li{
    padding: 10px 0;
}
.copyright{
    display: flex;
    justify-content: space-between;
    padding: 20px 0;
    margin: 0 100px;
}
.privacy{
    display: flex;
}z
.privacy p{
   padding: 0 10px;
}
</style>