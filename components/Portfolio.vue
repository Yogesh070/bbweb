<template>
<div class="container" id="portfolio">
    <div class="flex-container">
      <img src="svg/OrangeCircle.svg" alt="circle-vector">
    </div>
    <div class="content">
        <h2>Our Portfolio</h2>
        <p>Voice and Data Systems are crucial to the success or <br/>failure of most your businesses.</p>
    </div>
    <div class="slider-container" id="slider">
        <a href="https://www.behance.net/brandbuilder2021" target="_blank">
            <div class="slider behance" style="order:0" >
                <div class="slider-content"><h1>BEHANCE</h1></div>
            </div>
        </a>
        <a href="https://www.fiverr.com/brandbuildern" target="_blank">
            <div class="slider fiver" style="order:1">
                <div class="slider-content"><h1>FIVERR</h1></div>
            </div>
        </a>
        <a href="https://photos.google.com/share/AF1QipPfXGer1vw8FAACgkVRkHI51gcEiuxE5mt2DiIUNgUaoHGS8Diqt7xqKeuFqnWUrA?key=VVN6VjJWVG1qMWJoSmF5YS1zdTZSMzEzVXJyeG9n" target="_blank">
            <div class="slider drive" style="order:2"><div class="slider-content"><h1>Sample Designs</h1></div></div>
        </a>
    </div>
    <!-- <div class="button-group">
        <button @click="shift(-1)" class="prev-button">&laquo;</button>
        <button @click="shift(1)" class="next-button">&raquo;</button>
    </div> -->
</div>

</template>

<script>
    export default {
        methods: {
            shift(direction) {
                const slider = document.getElementById("slider");
                slider.children.forEach(function(sliderItem){
                const lastOrder = parseInt(sliderItem.style.order) ;
                const newOrder = (3 + direction + lastOrder) % 3 ;
                sliderItem.style.order = newOrder
                 + "" ;
        })
            },
        },
    }
</script>

<style lang="scss" scoped>
.slider-content{
    height: 100%;
    opacity: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: rgba(0, 0, 0, 0.63);
}
.slider-content:hover{
    opacity: 1;
    transition: all 300ms ease-in-out;
    h1{
        -webkit-text-stroke: 1px white;
        color: transparent !important;
        letter-spacing: 5px;
    }
}

.flex-container{
  display: flex;
  justify-content: center;

}
.container{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0 7vw;
    text-align: center;
    justify-content: center;
    min-height: 100vh;
}
.content{
    margin: 30px 0;
}
.slider-container{
    display: flex;
        // transition: 2s;
    justify-content: center;
    flex-wrap: wrap;
}
.slider{
        // height: 50px;
        // width: 240px;
        width: 22vw;
        margin: 20px;
        color: white;
        text-align: center;
        font-size: 20px;
        font-weight: 700;
         height: 200px; 
         height: 16vw;
         cursor: pointer;
        // transition: 2s;
}
  
.behance { background-image: url('/svg/behance.png'); background-size: cover;}
.fiver { background-image: url('/svg/fiver.png'); background-size: contain;}
.drive { background-image: url('/svg/drive.png'); background-size: cover;}


.button-group{ 
    button{
        width: 40px;
        font-size: 20px;
        color: white;
        border: none;
        padding: 10px;
        outline: none;
        cursor: pointer;
    }
}
.prev-button{
    background: $nav-color;
}
.next-button{
    background: $base-color;
}
@media (max-width: 660px){
    .slider{
        margin: 0;
        height: 85px;
        width: 80vw;
    }
    .flex-container{
          img{
      height: 80px;
    }
    }
}
</style>