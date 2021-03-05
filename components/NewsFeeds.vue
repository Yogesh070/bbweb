<template>
<div class="container" id="blog">
    <h2>News Feeds</h2>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Est, iusto!</p>
     <div class="parent">
        <div class="card" v-for="(item,index) in news" :key="index" data-aos="fade-down"
     data-aos-easing="linear"
     data-aos-duration="1000">
            <div>
                <img :src="item.thumbnail" :alt="item.title" srcset="">
            </div>
            <div>
                <h5>{{item.title}}</h5>
                <div class="author">
                    <div></div>
                    <p>{{`By ${item.author}`}}</p>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
data() {
    return {
        news:[{
            thumbnail:"/svg/Brand Builder (Color).svg",
            title:"Artificial Itelligence is Been common place in way",
            author:"Hari Thakur"
        },
        {
            thumbnail:"/svg/Brand Builder (Color).svg",
            title:"Artificial Itelligence is Been common place in way",
            author:"abc "
        },
        {
            thumbnail:"/svg/Design.svg",
            title:"Artificial Itelligence is Been common place in way",
            author:"Hari Thakur"
        },
        {
            thumbnail:"/svg/Discuss.svg",
            title:"Artificial Itelligence is Been common place in way",
            author:"Hari Thakur"
        },
        ]
    }
},
}
</script>

<style lang="scss" scoped>
.container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    margin: 80px 0;
}
.parent{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    margin: 50px 0;
}
.card{
    /* padding: 10px 30px; */
    min-height: 300px;
    min-width: 230px;
    padding: 20px;
    background-color: white;
    border-radius: 20px;
    box-shadow: 0 1px 18px rgba(0,0,0,.11);
    display: grid;
    grid-template-rows: 2fr 1fr;
    align-items: center;
    margin: 20px;
    p{
        padding: 20px 0;
    }
    img{
        height: 100px;
        width: 100px;
    }
    h3{
        margin-top: 18px;
    }
    
}
.card:hover{
    transform: scale(1.1);
}
.author{
    display: flex;
    justify-content: left;
    align-items: center;
    margin: 0px 20px;
    div{
        height: 20px;
        width: 20px;
        border-radius: 50%;
        padding: 0 0 0 5px;
        background: #A6C1F0;
    }
    p{
    font-size: 12px;
    font-weight: 700;
    margin-left: 10px;
}
}
</style>