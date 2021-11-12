<template>
  <div class="container">
      <div class="estimate-container" data-aos="zoom-in" data-aos-duration="2000">
          <h1>
              Grow Your Business<br/> With Us .
          </h1>
          <button class="primary-button btn-icon">
              <img src="/svg/arrow-right-solid.svg" alt="" id="arrow">
          Get Started</button>
      </div>
      <h1>
          Reach More Customer<br/> With Brand Builder
      </h1>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.btn-icon{
    display: flex;
    align-items: center;
}
#arrow{
    height: 20px;
    margin-right: 10px;
    color: white;
}
.container{
    background-image: url("/svg/Price estimation back design.svg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    height: 90vh;
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
        font-weight: 100;
    }
}
.container>h1{
    position: relative;
    top: 100px;
    /* margin-top: 100px; */
    text-align: center;
    color: white;
    font-weight: 100;
}
</style>