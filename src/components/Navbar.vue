<template>
  <header class="d-flex justify-content-around w-100">
    <div class="w-25">
      <router-link to="/">
        <img id="logo"
          :src="logo"
          :alt="alt"
        />
      </router-link>
    </div>
    <div class="w-50">
      <nav class="w-100 pt-5">
        <ul
          class="menu d-flex justify-content-between w-60 pt-4 fs-4 fw-bold text-light"
        >
          <router-link to="/" class="option">Home</router-link>
          <router-link to="/pedidos" class="option">Pedidos</router-link>
          <router-link to="/contact" class="option">Contact</router-link>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Navbar",
  props:['logo','alt']
};
</script>

<style scoped>
#logo {
  width: 170px;
  height: 150px;
  position: relative;
  top: 5%;
  left: 10%;
}

header {
  background-color: #ffffff;
  padding-bottom: 2%;
  border-bottom: 15px dashed red;
}
.menu {
  width: 100%;
}

.option {
  list-style: none;
  text-decoration: none;
  color: rgb(255, 0, 0);
  transition:0.5s;
}
.option:hover{
    color: #4e0101;
    transition:0.5s;
}
</style>
