<template>
<div style="background-color:#F7FAFF">
    <div class="progress-bar">
        <div class="line"></div>
        <div class="button-group">
            <!-- <button v-for="(tab,index) in process" :key="index"  v-bind:class="['tab-button', { active: currentTab === tab }]"
        v-on:click="currentTab = tab"><img :src="`/svg/SVG_Organized/Process/${tab}.svg`" :alt="tab" v-bind:class="{activeImg: currentTab === tab}">
        </button> -->
        <div class="btn" v-for="(tab,index) in process" :key="index"  v-bind:class="['tab-button', { active: currentTab === tab }]"
        v-on:click="currentTab = tab">
            <img :src="`/svg/SVG_Organized/Process/${tab}.svg`" :alt="tab" v-bind:class="{activeImg: currentTab === tab}"> 
            <p class="btn-text">{{tab}}</p>
        </div>
        </div>
    </div>
    <div>
    <component :is="currentTabComponent" class="tab"></component>
    </div>
</div>
</template>

<script>
import Planning from '@/components/Planning.vue';
import Sketch from '@/components/Sketch.vue';
export default {
data(){
  return{
    currentTab: "Planning",
    process:['Discuss','Planning','Sketch','Design','Development','Deliver'],
  }
},
computed: {
  currentTabComponent: function() {
  return this.currentTab;
  }
},
components:{
  Planning,
  Sketch,
},
}
</script>

<style lang="scss" scoped>
.progress-bar{
    padding: 70px 0 0 0;
    position: relative;
    top: 55px;
}
.line{
    position: absolute;
    height: 2px;
    width: 100%;
    background: #D5E1FF;
    top: 32px;
}
.button-group{
    display: flex;
    justify-content: space-around;
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
}
// .progress-bar::after{
//    content: '';
//   position: absolute;
//   width: 6px;
//   height: 91vh;
//   top: -430px;
//   background-color: #D5E1FF;
//   bottom: 0;
//   left: 50%;
//   margin-left: -3px;
//   transform: rotate(90deg);
    
// }
@keyframes rotateIcon {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
}
.btn-text{
    position: absolute;
    top: 75px;
    color: $base-color;
    font-size: 16px;

}
.tab-button img:hover{
    animation-name: rotateIcon;
    animation-duration: 1.5s;
}
.tab-button{
    border: none;
    cursor: pointer;
    padding: 20px;
    border-radius: 50%;
    border: 1px solid $base-color;
    background-color: #F7FAFF;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 66px;
    z-index: 100;
}
.activeImg{
  filter: invert(43%) sepia(97%) saturate(2339%) hue-rotate(5deg);

}
.active{
    box-shadow: 0 1px 18px rgba(0,0,0,.11);
    color: $secondary-color;
    border: none;
    background: white;
}
button:focus{
    outline: none;
}
img{
    height: 20px;
    width: 25px;
}
@media (max-width:660px){
    .progress-bar{
        top: 35px;
        padding: 0;
    }
    .line{
        display: none;
    }
    .tab-button{
        min-height: 57px;
        padding: 15px;
    }
    .button-group{
        position: relative;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        justify-items: center;
        grid-row-gap: 15px;
    }
    .btn-text{
        display: none;
    }
}
</style>