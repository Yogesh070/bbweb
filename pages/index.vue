<template>
  <div>
    <Header/>
    <!-- <Navbar/> -->
    <Newnavbar/>
    <div class="hero-container">
        <div data-aos="fade-right"  data-aos-duration="3000">
          <p>We Develop Creative Product</p>
          <h1>
            We Are Creative <br/>& Minimalist
          </h1>
          <button class="primary-button">Get Started</button>
          <button class="secondary-button">Intro Video</button>
      </div>
        <img src="/svg/Man Floating.svg" alt="">
    </div>
    <Services/>
    <Estimate/>
    <!-- <Slider/> -->
    
    <Portfolio/>
    <Process/>
    <NewsFeeds/>
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
  // Newnavbar,
  // Slider
},
}
</script>

<style lang="scss" scoped>
.hero-container{
  /* height:100vh; */
  display: grid;
  grid-template-columns: 1fr 1fr;
  justify-items: center;
  align-items: center;
  // margin: 30px 0;
  margin: 4vw 7vw;
  h1{
    font-size: 5vw; 
    margin: 10px 0 30px 0;
  }
}

@media (max-width:820px)  { 
    .hero-container{
        grid-template-columns: 1fr  1fr;
    }
}
@media (max-width:1024px){
  .hero-container{
    img{
      max-width: 350px;
      min-width: 200px
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