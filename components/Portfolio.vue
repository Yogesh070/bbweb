<template>
<div class="container" id="portfolio">
    <div class="content">
        <h2>Our Portfolio</h2>
        <p>Voice and Data Systems are crucial to the success or <br/>failure of most your businesses.</p>
    </div>
    <div class="slider-container" id="slider">
        <div class="slider green" style="order:0" >1</div>
        <div class="slider blue" style="order:1">2</div>
        <div class="slider grey" style="order:2">3</div>

    </div>
    <div class="button-group">
        <button @click="shift(-1)" class="prev-button">&laquo;</button>
        <button @click="shift(1)" class="next-button">&raquo;</button>
    </div>
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
.container{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 4vw 7vw;
    text-align: center;
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
        // transition: 2s;
}
.green { background: #1abc9c; }
.blue { background: #3498db; }
.grey { background: #34495e; }

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

}
</style>