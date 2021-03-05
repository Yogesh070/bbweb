<template>
  <div class="container">
      <div>
        <h2>Our Cool Organize <br/>Sketch Process</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda, cupiditate!</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam nemo asperiores neque repellendus accusamus et dolorum adipisci repellat expedita minus.</p>
        <button>Learn More</button>
      </div>
      <div>
          <img src="svg/Digital Marketing.svg" alt="">
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.container{
    display: grid;
    grid-template-columns: 2fr 1fr;
    padding: 50px;
    background-color: #F7FAFF;
    margin-top: 50px;
}
.container p{
    padding: 15px 0;
}
img{
    min-height: 400px;
}
button{
    background-color: #EE6B04;
    border: none;
    padding: 13px 16px;
    color: wheat;
    font-weight: 700;

}
</style>