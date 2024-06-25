<template>
  <div class="d-flex justify-content-around banner ">

            <img  class="pizza  order-2 " src="/imgs/pizza-main.png" alt="">


            <div class="   left text-center d-flex  flex-column align-self-center   ">
                    <p>
                        <H1 class="text-danger fw-bold " >The best pizza of the Galaxy </H1>
                    </p>
                    <div>
                        <button class="btn ">Make a Order</button>
                    </div>
            </div>
          
        </div>

</template>

<script>
export default {
    name:'Banner'
}
</script>





<style scoped>
.pizza {
  width: 36%;
  position: relative;
  filter: drop-shadow(0px 0px 25px black);
  animation: rodar 17s infinite linear;
}

@keyframes rodar {
  0% {
    transform: rotateZ(0deg);
  }

  100% {
    transform: rotateZ(360deg);
  }
}

.btn {
  background-color: #ce0101;
  color: #ffffff;
}
.banner{
background-image: url('/public/imgs/334.jpg');  
  background-color: black;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  background-attachment: fixed;
  /*  font-family: "Pizza"; */
}
h1 {
  font-size: 4rem;
  text-shadow: 0px 5px 15px black;


    -webkit-text-stroke: 1px white; 
}
</style>