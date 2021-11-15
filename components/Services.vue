<template>
<div class="container" id="services">
    <div class="flex-container">
      <img src="/svg/OrangeCircle.svg" alt="circle-vector">
    </div>
    <h2>Our Services</h2>
    <p>Voice and Data Systems are crucial to the success or failure of most businesses.</p>
     <div class="parent">
        <div class="card" v-for="(service,index) in services" :key="index" id="show-modal" @click="showModal = true, activeIndex=index" :class="'card-'+index">
            <div>
                <img :src="`/svg/SVG_Organized/Our_Services/${service.title}.svg`" :alt="service" srcset="">
                <h3>{{service.title}}</h3>
                <p><span v-html="service.desc.split('|').join('<br>')"></span></p>

                <a id="show-modal" @click="showModal = true, activeIndex=index" >Read More</a>
            </div>
        </div>
    </div>
        <Modal v-if="showModal" @close="showModal = false" :activeOption="activeIndex" :service="services">
      </Modal>
</div>
</template>

<script>
import Modal from '@/components/Modal.vue';
export default {
data() {
    return {
        services:[
            {
                title:"Product Design",
                desc:"Website| Mobile App| Social Media ",
                summary:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Earum, beatae recusandae. Reprehenderit quos fuga recusandae. Sunt voluptatibus eum commodi! Minima repellendus mollitia, quod perspiciatis praesentium repudiandae, ratidi soluta maiores omnis ullam est itaque nam ipsam cum quas, eius aut nisi officiis qui officia veniam. Dolorem, voluptates animi?"
            },
            {
                title:"Digital Marketing",
                desc:"SEO (Search Engine Optimization)| Social Media Marketing| Graphics Design",
                summary:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Earum, beatae recusandae. Reprehenderit quos fuga recusandae. Sunt voluptatibus eum commodi! Minima repellendus mollitia, quod perspiciatis praesentium repudiandae, ratione facere sapiente modi soluta mallam est itaque nam ipsam cum quas, eius aut nisi officiis qui officia veniam. Dolorem, voluptates animi?"
            },
            {
                title:"Business Planning",
                desc:"We design, develop, integrate and deploy various software as a service ",
                summary:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Earum, beatae recusandae. Reprehenderit quos fuga recusandae. Sunt voluptatibus eum commodi! Minima repellendus mollitia, quod perspiciatis praesentium repudiandae, ratione facere sapiente modi soluta maiores omnis ullam est itaque nam ipsam cum quas, eius aut nisi officiis qui officia veniam. Dolorem, voluptates animi?"
            },
        ],
        showModal:false,
        activeIndex:Number,
    }
},
components: {
    Modal,
},
}
</script>

<style lang="scss" scoped>
.flex-container{
  display: flex;
  justify-content: center;
}
.container{
    text-align: center;
    margin: 10px 4vw 7vw 4vw;
}
.parent{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    justify-content: center;
    grid-gap: 20px;
    text-align: center;
    min-width: 900px;
    margin: 50px auto;
    max-width: 1024px;
}
#services>p{
    max-width: 500px;
    margin: auto;
}
.card{
    /* padding: 10px 30px; */
    min-height: 330px;
    min-width: 300px;
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
    cursor: pointer;
    p{
        padding: 20px 0;
        font-size: 14px;
        max-width: 250px;
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
    cursor: pointer;
    }
}

.card:hover{
    transform: translateY(10px);
    transition: transform 1s ease ;
    border-bottom: 4px solid $base-color;
}
@media (max-width:1120px)  { 
    .container{
    margin: 4vw 5vw;
    }
}
@media (max-width:1024px)  { 
    .parent{
        grid-template-columns: 1fr 1fr;
        min-width: 0;
    }
    .card-2{
    grid-column: 1/3;
    }
}
@media (max-width:600px)  { 
    .parent{
        margin: 50px;
        grid-template-columns: 1fr;
    }
    .card-2{
    grid-column: 1;
    }
    .flex-container{
        img{
      height: 80px;
    }
    }
}
</style>