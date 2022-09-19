<script>
import axios from "axios";
import { onBeforeMount } from "vue";
// import { onBeforeMount, reactive } from "vue";

import CardProcurado from '../components/CardProcurado.vue'

export default {
  components: { CardProcurado }, 
  data() {
    return {
      data: []
    }
  },
  async created() {
    const {data} = await axios.get('https://api.fbi.gov/wanted/v1/list')
    console.log(data)
    this.data = data.items
    console.log(this.data)

  }
}
// let data = reactive([])
// onBeforeMount(() => {
// })
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
      <card-procurado v-for="procurado of data" :key="procurado.uid" :procurado="procurado"  />

    </div>
  </div>
</template>
<style>
.card {
  padding: 6%;
  margin-left: 10%;
  display: flex;
  flex-wrap: wrap;
}

.name {
  font-family: Arial, Helvetica, sans-serif;
  margin-top: 15%;
  width: 150px;
}

.onecard {
  font-size: 15px;
  border: solid 2px #0a0a12;
  border-radius: 15px;
  width: 140px;
  height: 340px;
  padding: 15px;
  margin: 2%;
  box-shadow: 0px 5px 10px 0 rgba(0, 0, 0, 0.438);
}

.onecard img {
  display: flex;
  width: 22px;
  border-radius: 15px;
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
