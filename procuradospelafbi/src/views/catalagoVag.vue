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
  </div>
</template>
<style>
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
.link a{
    text-decoration: none;
    color: #0a0a12;
}
.categorias {
  display: flex;
  align-items: center;
  justify-content: center;
}
.categorias a{
    color: black;
}
.categorias span {
  margin: 0 4%;
}

</style>
