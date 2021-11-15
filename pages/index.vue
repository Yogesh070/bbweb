<template>
  <div class="scrollbar">
    <Header/>
    <!-- <Navbar/> -->
    <Newnavbar/>
    <div class="hero-container">
        <div data-aos="fade-right"  data-aos-duration="3000">
          <p>We Develop Creative Product</p>
          <h6>
            We Are Creative <br/>& Minimalist
          </h6>
          <button class="primary-button">Get Started</button>
          <button class="secondary-button">Intro Video</button>
      </div>
        <img src="/svg/Man Floating.svg" alt="floating svg" class="float" srcset="/svg/Man Floating.svg /svg/Man Floating@2x.png 2x">
    </div>
    <img src="/svg/Half Hand.svg" alt="half-hand" id="half-hand">
    <Services/>
    <Estimate/>
    <Clients/>
    <!-- <Slider/> -->
    
    <Portfolio/>
    <Process/>
    <!-- <NewsFeeds/> -->
    <Footer/>
    
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Navbar from '@/components/Navbar.vue';
import Process from '@/components/Process.vue';
import NewsFeeds from '@/components/NewsFeeds.vue';
import Footer from '@/components/Footer.vue';
import Services from '@/components/Services.vue';
import Estimate from '@/components/Estimate.vue';
import Portfolio from '@/components/Portfolio.vue';
import Clients from '@/components/Clients.vue';
// import Slider from '@/components/Slider.vue';
export default {
components: {
  Header,
  Navbar,
  Process,
  NewsFeeds,
  Footer,
  Services,
  Estimate,
  Portfolio,
  Clients
  // Newnavbar,
  // Slider
},
}
</script>

<style lang="scss" scoped>
    #half-hand{
      position: absolute;
      height: 500px;
      top: 700px;
      z-index: -2;
    }
  .float {
    transition: Floating 6s ease-in-out 1s;
    animation: 6s ease-in-out 1s infinite reverse both running Floating;
    animation-name: Floating;
    animation-duration: 6s;
    animation-iteration-count: infinite;
    animation-timing-function: ease-in-out;
    -webkit-animation-name: Floating;
    -webkit-animation-duration: 6s;
    -webkit-animation-iteration-count: infinite;
    -webkit-animation-timing-function: ease-in-out;
  }
  @keyframes Floating {
    from {
      transform: translate(0, 0px);
    }
    65% {
      transform: translate(0, 30px);
    }
    0% {
      transform: translate(0, -0px);
    }
  }
  @-webkit-keyframes Floating {
    from {
      -webkit-transform: translate(0, 0px);
    }
    65% {
      -webkit-transform: translate(0, 30px);
    }
    to {
      -webkit-transform: translate(0, -0px);
    }
  }
.hero-container{
  /* height:100vh; */
  display: grid;
  grid-template-columns: 2fr 1fr;
  justify-items: center;
  align-items: center;
  // margin: 30px 0;
  margin: 4vw 7vw;
  position: relative;
  h1{
    font-size: 137px;
    font-weight: 100;
    /* font-size: 5vw;  */
    margin: 10px 0 30px 0;
  }
  h6{
    font-size: 90px;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem 0 3rem 0;
    color:#253E72 ;
  }
}

@media (max-width:1024px){
  .hero-container{
    img{
      max-width: 350px;
      min-width: 200px
    }
    h6{
      font-size: 70px;
    }
  }
}
@media (max-width:820px)  { 
    .hero-container{
        grid-template-columns: 1fr  1fr;
        h6{
          font-size: 60px;
        }
        img{
          height: 325px;
        }
    }
}
@media (max-width:600px)  { 
    .hero-container{
        h6{
          font-size: 48px;
        }
    }
}
@media (max-width:540px)  { 
    .hero-container{
        grid-template-columns: 1fr;
        // font-size: 72px;
        h1{
          font-size: xxx-large;
        }
        img{
          display: none;
        }
    }
}
</style>