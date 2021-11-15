<template>
  <div class="container">
      <img v-for="(client,index) in clients" :key="index" :src="client['image'][0]" :alt="'client'+index" :srcset="client['image'][1]+' 2x'">
  </div>
</template>

<script>
export default {
    data(){
        return{
            clients:[
                {image:['/clients/aestheticMakeupLogo.png','/clients/aestheticMakeupLogo@2x.png']},
                {image:['/clients/bigbellLogo.png','/clients/bigbellLogo@2x.png']},
                {image:['/clients/veda.png','/clients/veda@2x.png']},
                {image:['/clients/axon.png','/clients/axon@2x.png']},
                {image:['/clients/soch_logo_new.png','/clients/soch_logo_new@2x.png']},
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .container{
        margin: 4vw 7vw;
        display: grid;
        grid-template-columns: repeat(5,1fr);
        align-items: center;
        justify-items: center;
        margin-bottom: 0;
        img{
            align-self: center;
            height: 200px;
        }
    }
    @media (max-width:1024px){
    .container{
        img{
        height:65px;
        }
    }
    }
</style>