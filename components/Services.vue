<template>
<div class="container" id="services">
    <h2>Our Services</h2>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Est, iusto!</p>
     <div class="parent">
        <div class="card" v-for="(service,index) in services" :key="index" data-aos="flip-up" data-aos-duration="2000">
            <div>
                <img :src="`/svg/SVG_Organized/Our_Services/${service}.svg`" :alt="service" srcset="">
                <h3>{{service}}</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Libero debitis ut consequatur.</p>
                <a href="#">Read More</a>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
data() {
    return {
        services:["Product Design", "Digital Marketing","Business Planning"]
    }
},
}
</script>

<style lang="scss" scoped>
.container{
    // display: flex;
    // flex-direction: column;
    // justify-content: center;
    text-align: center;
    margin: 4vw 7vw;
}
.parent{
    // display: flex;
    // justify-content: center;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    justify-items: center;
    // align-items: center;
    // justify-items: center;
    grid-gap: 20px;
    text-align: center;
    margin: 50px 0;
}
.card{
    /* padding: 10px 30px; */
    min-height: 330px;
    min-width: 230px;
    background-color: white;
    border-radius: 20px;
    box-shadow: 0 1px 18px rgba(0,0,0,.11);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    // margin: 20px;
    padding: 20px;
    p{
        padding: 20px 0;
        font-size: 14px;
    }
    img{
        height: 130px;
        width: 130px;
    }
    h3{
        margin-top: 18px;
    }
    a{
    color: $secondary-color;
    text-decoration: none;
    }
}
.card:hover{
    transform: translateY(30px);
    transition: transform 1s ease ;
    border-bottom: 4px solid $base-color;
}
@media (max-width:820px)  { 
    .parent{
        grid-template-columns: 1fr 1fr;
    }
}
@media (max-width:540px)  { 
    .parent{
        grid-template-columns: 1fr;
    }
}
</style>