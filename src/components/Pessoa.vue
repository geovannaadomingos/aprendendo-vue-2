<!-- componente que vai descrever uma pessoa -->
<template>
    
    <img :src="imagem_perfil" alt="imagem de perfil">
    <!-- demonstrando hierarquia de componentes com a utilização do componente Info -->
    <Info/>

</template>
<script>
import Info from './Info.vue'
export default {
    name: "Pessoa",
    data() {
        return{
            imagem_perfil:"https://avatars.githubusercontent.com/u/53124770?v=4",
        }
    },
    components: { Info }
}
</script>