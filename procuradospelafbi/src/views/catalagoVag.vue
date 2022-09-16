<script setup>
import axios from "axios";
import { onMounted } from "vue";

let data = []
onMounted(() => {
  axios.get('https://api.fbi.gov/wanted/v1/list').then(res => {
    data = res.data.items
    console.log(data)
  })
})
</script>
<template>
  <div class="main">
    <div class="lista">
      <h2 class="txtprin">Mais Procurados</h2>
      <hr />
      <div class="categorias">
        <router-link class="link" to="/cadavag">
          <span>Terrorismo</span>
        </router-link>
        <span>Fugitivos</span>
        <span>Desaparecidos</span>
      </div>
    </div>
    <div class="card">
      <div class="onecard">
        <img src="../img/preview.jpeg">
        <div class="name">
          <h4>Causa</h4>
          <p>name</p>
        </div>
      </div>
      <div class="onecard">
        <img src="../img/preview.jpeg">
        <div class="name">
          <h4>Causa</h4>
          <p>name</p>
        </div>
      </div>
      <div class="onecard">
        <img src="../img/preview.jpeg">
        <div class="name">
          <h4>Causa</h4>
          <p>name</p>
        </div>
      </div>
      <div class="onecard">
        <img src="../img/preview.jpeg">
        <div class="name">
          <h4>Causa</h4>
          <p>name</p>
        </div>
      </div>
      
      
    </div>
  </div>
</template>
<style>
.card {
  padding: 6%;
  margin-left: 15%;
  display: flex;
}

.name {
  font-family: Arial, Helvetica, sans-serif;
  width: 10%;
  margin-top: 10%;
  margin-left: 30%;
}

.onecard {
  border: solid 2px #000;
  border-radius: 15px;
  width: 140px;
  height: 240px;
  padding: 15px;
  margin: 2%;
}

.onecard img {
  width: 100%;
}

.txtprin {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 1.5%;
  font-family: Arial, Helvetica, sans-serif;
  font-weight: bold;
  color: #0a0a12;
  font-size: 2em;
  margin-right: 14.5%;
}

.link a {
  text-decoration: none;
  color: #0a0a12;
}

.categorias {
  display: flex;
  align-items: center;
  justify-content: center;
}

.categorias a {
  color: black;
}

.categorias span {
  margin: 0 4%;
}
</style>
