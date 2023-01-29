<template>
  <div class="header">
    <div>
      <img src="svg/Email.svg" alt="email-icon">
      <a href="mailto:mail@brandbuilder.com.np">mail@brandbuilder.com.np</a>
      <img src="svg/Phone.svg" alt="phone-icon">
      <a href="tel:+9779816162091">9816162091</a>
    </div>
      
      <div class="socials">
        <ul>
          <li v-for="social in socials" :key="social.name">
          <a :href="social.link" target="_blank">
            <img :src="`svg/${social.icon}`" :alt="social.name">
          </a>
        </li>
        </ul>
      </div>
      <div class="call-card">
        <span>Get a Call</span>
        <h5>9816162091</h5>
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
                link:"https://www.facebook.com/brandbuildernepal"
            },
            {
                icon:"Instagram.svg",
                name:"instagram",
                link:"https://www.instagram.com/brandbuilder.nepal"
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
    padding: 10px 0;
    border-bottom: 1px solid #616368;
    display: grid;
    grid-template-columns: 1fr 1fr;
    justify-items: center;
    position: relative;
    a{
      text-decoration: none;
      color: #616368;
    }
    .phno{
      color: #616368;
    }
}
.call-card{
    position: absolute;
    right: 60px;
    text-align: center;
    background: $base-color;
    color: white;
    height: 75px;
    top: 0;
    width: 200px;
    h5{
      font-size: 30px;
      // padding: 15px;
      color: white;
    }
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
@media (max-width:660px){
  .header{
    display: none;
  }
}
@media (max-width:1300px){
  .call-card{
    display: none;
  }
}
</style>