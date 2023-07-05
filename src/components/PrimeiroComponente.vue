<template>
  <div>
    <h1>Olá, mundo!</h1>
    <p>
      {{ texto }}
    </p>
  </div>
    
</template>

<script>
// exportando para poder utilizar esse elemento, cujo nome é PrimeiroComponente, em outros lugares (como no App.vue)
export default ({
  name: "PrimeiroComponente",
  // os componentes podem conter dados. Para adicioná-los, utilizamos os inicializamos  dentro de uma função chamada data
  data(){
    return{
      texto: "Esse é o texto inicial"
    }
  }
})
</script>