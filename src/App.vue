<template>
  <Navbar :logo="logo_src" :alt="app_name" />
  <router-view />

  
  <Footer />
</template>

<style></style>

<script>
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";

export default {
  components: {
    Navbar,
    Footer,
  },
  data() {
    return {
      logo_src: "/imgs/pizza-planet2.jpg",
      app_name: "Pizza Planet",
    };
  },
};
</script>


<style >
body{
  overflow-x:hidden ;
  font-family: 'Pizza';
}

@font-face {
  font-family: 'Pizza';
  src: url('/public/fonts/pizza.ttf');
}

.main-conteiner{
  width: 100%;
  
  margin-bottom: 5%;
 
}
  
</style>