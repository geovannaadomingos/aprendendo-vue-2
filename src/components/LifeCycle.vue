<template>
    <h1>
        Meu nome é: {{ nome }}
    </h1>
</template>

<script>
export default {
    name:"LifeCycle",
    data(){
        return{
            nome: "nenhum nome, ainda"
        }
    },
    created(){
        // utilizando a função de setTimeOUt para adicionar o tempo de 1 segundo antes da alteração do atributo nome durante a criação do componente
        setTimeout(()=>{
            this.nome = "Geovanna" 
        },1000)
    },
    mounted(){
        // utilizando a função de setTimeOUt para adicionar o tempo de 2 segundos antes da alteração do atributo nome durante a montagem do componente
        setTimeout(()=>{
            this.nome = "Geovanna Domingos" 
        },2000)
    }
}
</script>