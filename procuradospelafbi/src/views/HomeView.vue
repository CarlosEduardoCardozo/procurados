<script setup></script>

<template>
  <div class="bemvindo">
    <span>BEM VINDO(A) A NOSSA ÁREA DAS PESSOAS MAIS PROCURADAS PELO FBI</span>
    <router-link class="btnenter" to="/list"><button>Acesse a lista</button></router-link>
  </div>
</template>
<style>
.bemvindo {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 15%;
  color: #0a0a12;
  font-size: 1.8rem;
  font-family: Arial, Helvetica, sans-serif;
  font-weight: bold;
  margin-bottom: 20%;
}

.bemvindo button {
  padding: 15px;
  border-radius: 25px;
  text-decoration: none;
  border: none;
  min-width: 140px;
  cursor: pointer;
  background-color: #0a0a12;
  margin-top: 15px;
}
.btnenter a{
  color: #fff;
}
.btnenter button{
  color: #fff;
}
</style>