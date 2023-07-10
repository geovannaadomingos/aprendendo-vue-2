<!-- Apesar de App.vue não estar na pasta d ecomponentes, ele também é considerado uma entidade de componente -->
<template>
  <div>
    <!-- o componente também poderia ser utilizado utilizando "primeiro-componente" -->
    <PrimeiroComponente />
    <h3>{{ textoQualquer }}</h3>
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
// importando componentes
import PrimeiroComponente from './components/PrimeiroComponente.vue';
import LifeCycle from './components/LifeCycle.vue';
import Pessoa from './components/Pessoa.vue';

// exportando para poder utilizar esse elemento, cujo nome é App, em outros lugares (como no main.js)
export default {
  name: "App",
  // adicionando um objeto componentes para serem usados nesse elemento
  components:{
    PrimeiroComponente,
    LifeCycle,
    Pessoa
  },
  // Por mais que esse elemento App sirva, sobretudo, para abrigar outros componentes (isto é, ele é o componentes root da aplicação), ele também pode conter atributos e metodos dentro dele
  data(){
    return{
      textoQualquer: "Algumas outras informações sobre mim:"
    }
  }
}
</script>

<!-- utilizando estilização global-->
<style>
  body{
    background-color: bisque;
  }

</style>
