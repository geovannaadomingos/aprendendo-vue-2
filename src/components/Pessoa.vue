<!-- componente que vai descrever uma pessoa -->
<template>
    <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
    <!-- demonstrando hierarquia de componentes com a utilização do componente Info -->
    <Info/>

</template>
<script>
import Info from './Info.vue'
export default {
    name: "Pessoa",
    data() {
        return{
            nome: "Geovanna"
        }
    },
    components: { Info }
}
</script>