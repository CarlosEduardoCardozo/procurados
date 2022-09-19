<script>
    export default {
        props: {
            procurado: {
                type: Object
            }
        }
    }
</script>
<template>
    <div class="onecard">
        <img :src="procurado.images[0].original">
        <div class="name">
          <h4>{{procurado.subjects[0]}}</h4>
          <p>{{procurado.title}}</p>
        </div>
      </div>  
      
</template>