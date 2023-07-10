<template>
    <div>
        <!-- utilizando a diretiva v-if para tornar a tela dinâmica e condicionar o aparecimento de informações. Essa diretiva pode estra sozinha, ou vir acompanhada da diretiva else, logo abaixo-->
        <p v-if="esta_trabalhando">No momento, estou trabalhando com as seguintes tecnologias:</p>
        <p v-else>Estudo as seguintes tecnologias:</p>
        <!-- Utilizando a diretiva v-for para exibir os elementos de um array (tecnologias) que está no script da página-->
        <ul>
            <li v-for="(tecnologia, index) in tecnologias" v-bind:key="index">{{tecnologia}}</li>
        </ul>
        <p>Algumas das minhas habilidades pessoais são:</p>
        <!-- Utilizando a diretiva v-for para exibir os elemento de array de objetos -->
        <ul>
            <li v-for="elemento in habilidades_pessoais" :key="elemento.id"> {{ elemento.habilidade }}</li>
        </ul>
        <div>
            <!-- utilizando a diretiva click para executar um método -->
            <button @click="show_email">{{texto_botao}}</button>
        </div>
        <!-- diferentemente do if,v-bind:href="meu_link"  a diretiva v-show não tem uma alternativa, ou seja, não tem um else. Mostra ou não mostra, sem o caso se mostrar algo alternativo  -->
        <p v-show="mostrar_email">E-mail: {{email}}</p>

        <!--  utilizando a diretiva v-bind para pegar dinamicamente o valor do href     -->

        <p>Para ver mais informções sobre mim, acesse o meu  <a v-bind:href="linkedin" target="_blank" >LinkedIN</a></p>
        
    </div>
     
</template>
<script>
export default {
    name:"Info",
    data(){
        return{
            esta_trabalhando: true,
            mostrar_email: false,
            email: "gmdomingosn@gmail.com",
            linkedin:"https://br.linkedin.com/in/geovanna-domingos-b31b79190",
            texto_botao: "Mostrar e-mail",
            tecnologias: ["JavaScript", "React.js", "TypeScript", "HTML", "CSS", "Git", "Python"],
            habilidades_pessoais:[
                {id: 1, habilidade:"Comunicação"},
                {id: 2, habilidade:"Trabalho em equipe"},
                {id: 2, habilidade:"Proativade"}
            ]
        }
    },
    methods:{
        show_email(){
            this.mostrar_email = !this.mostrar_email
            if(this.mostrar_email){
                this.texto_botao = "Esconder e-mail"
            }
        }
    }
}
</script>