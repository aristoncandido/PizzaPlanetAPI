<template>
  <div class="text-center">
    <p>Componente de Mensagem</p>
    <div>
      <form id="pizza-form text-center ">
        <div class="input-container">
          <label for="nome" class="text-danger fw-bold fs-5">Seu nome :</label>
          <input
            type="text"
            id="nome"
            v-model="nome"
            name="nome"
            placeholder="Digite seu nome"
          />
        </div>
        <div class="input-container">
          <label for="massa" class="text-danger fw-bold fs-5"
            >Escolha sua massa:</label
          >
          <select name="massa" id="massa" v-model="massa">
            <option value="">Selecione sua massa</option>
            <option value="fina">Massa Fina</option>
          </select>
        </div>
        <div class="input-container">
          <label for="molho" class="text-danger fw-bold fs-5"
            >Escolha seu molho:</label
          >
          <select name="molho" id="molho" v-model="molho">
            <option value="">Selecione seu molho</option>
            <option value="tomate">Tomate</option>
          </select>
        </div>
        <div class="input-container">
          <label for="cobertura" class="text-danger fw-bold fs-5"
            >Selecione a cobertura:</label
          >
          <div class="checkbox-container">
            <input
              type="checkbox"
              name="cobertura"
              v-model="cobertura"
              value="cobertura"
            />
            <span class="text-warning pb-1">Calabresa</span>
          </div>
        </div>
        <div class="input-container">
          <input
            type="submit"
            class="submit-btn btn btn-danger"
            value="Make a pizza!"
          />
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "PizzaForm",
  data(){
    return{
        massas:null, //dados no plural
        molhos:null,
        coberturasdata:null,


        massa:null, //dado proriamente dito (singular)
        molho:null,
        coberturas:null,
       
        status:'Solicitado',
        msg:null
        
    }


    },
        methods: {
        async getIngredients(){

            //busca a rota ingredientes
            const req = await fetch("http://localhost:3000/ingredientes");
            const data = await req.json();

            console.log(data);



        },

        mounted() {
            this.getIngredients()
        },
  }
};
</script>

<style scoped>
.input-container {
  margin: 15% auto;
  text-align: start;
  display: flex;
  justify-content: space-around;
  flex-direction: column;
}

label {
  border-left: 5px solid red;
  padding-left: 5%;
  margin-bottom: 6%;
}
</style>
