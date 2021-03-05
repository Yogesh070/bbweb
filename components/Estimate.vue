<template>
  <div class="container">
      <div class="estimate-container" data-aos="zoom-in" data-aos-duration="2000">
          <h1>
              Estimate Your Project <br/> & Say Hi Here.
          </h1>
          <button class="primary-button">
              <!-- <img src="/svg/SVG_Organized/arrow.svg" alt=""> -->
          Get Started</button>
      </div>
      <h1>
          Your Businesss Is Unique<br/> Need a Platform?
      </h1>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.container{
    background-image: url("/svg/Price estimation back design.svg");
    background-size: cover;
    background-repeat: no-repeat;
    // background-position: center;
    height: 70vh;
}
.estimate-container{
    background-color: #F8F8F8;
    background-image: url("/svg/Currencies.svg");
    background-size: contain;
    background-position: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 60px;
    margin: 0 auto;
    max-width: 800px;
    border-radius: 40px;
    box-shadow: 0 1px 18px rgba(0,0,0,.11);

    h1{
        padding: 20px;
    }
}
.container>h1{
    margin-top: 100px;
    text-align: center;
    color: white;
}
</style>