<template>
  <main class="home main-conteiner">
    <Banner />

    <div class="formulario flex-column">
      <h3 class="text-danger fw-bolder" >Make your Order</h3>
      <PizzaForm />
    </div>
  </main>
</template>

<script>
import Banner from "../components/Banner.vue";
import PizzaForm from "../components/PizzaForm.vue";

export default {
  name: "Home",
  components: {
    Banner,
    PizzaForm,
  },
};
</script>

<style scoped>
.formulario {
  width: 100%;

  margin-bottom: 10%;
  padding-top: 5%;
  display: flex;

  align-items: center;
  justify-content: center;
  border-top: 15px dashed red;
}
</style>
