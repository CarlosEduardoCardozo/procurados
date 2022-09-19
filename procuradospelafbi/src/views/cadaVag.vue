<script>
    import axios from "axios";
    import { onBeforeMount } from "vue";
    // import { onBeforeMount, reactive } from "vue";
    
    import cardSepardoProc from '../components/cardSepardoProc.vue'
    
    export default {
      components: { cardSepardoProc }, 
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

</script>
<template>
    <cardSepardoProc v-for="procurado of data" :key="procurado.uid" :procurado="procurado"  />
    <div class="main">
        <div class="lista">
            
            <h2 class="txtprin">Mais Procurados</h2>
            <hr>
            <div class="categorias">
                <span>Terrorismo</span>
                <span>Fugitivos</span>
                <span>Desaparecidos</span>
            </div>
        </div>
    </div>
    <div class="previa">
        <div class="img">
            <img src="../img/preview.jpeg" alt="">
        </div>
        <div class="infos">
            <h2>ABDELKARIM HUSSEIN MOHAMED AL-NASSER</h2>
            <p>Conspiracy to Kill U.S. Nationals; Conspiracy to Murder U.S. Employees; Conspiracy to Use Weapons of Mass Destruction Against U.S. Nationals; Conspiracy to Destroy Property of the U.S.; Conspiracy to Attack National Defense Utilities; Bombing Resulting in Death; Use of Weapons of Mass Destruction Against U.S. Nationals; Murder While Using Destructive Device During a Crime of Violence; Murder of Federal Employees; Attempted Murder of Federal Employees</p>
        </div>
        <div class="ttimg">
            <img src="../img/tt.png" alt="">
        </div>
        
    </div>
</template>
<style>
.txtprin{
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

.categorias{
    display: flex;
    align-items: center;
    justify-content: center;
}
.categorias span{
    margin: 0 4%;
}
.previa{
    display: flex;
    padding: 5%;
    margin-left: 10%;
}
.infos{
    width: 30%;
    font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    margin-left: 80px;
    margin-right: 240px;
}
.previa img {
    margin-left: 20px;
    width: 90%;
    border-radius: 20px;
    box-shadow: 0 0 10px 0 #000;
}
</style>