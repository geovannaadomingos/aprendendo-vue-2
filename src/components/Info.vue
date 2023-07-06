<template>
    <div>
        <!-- utilizando a diretiva v-if para tornar a tela dinâmica e condicionar o aparecimento de informações. Essa diretiva pode estra sozinha, ou vir acompanhada da diretiva else, logo abaixo-->
        <p v-if="esta_trabalhando">No momento, estou trabalhando com as seguintes tecnologias:</p>
        <p v-else>Estudo as seguintes tecnologias:</p>
        <ul>
            <li>JavaScript</li>
            <li>TypeScript</li>
            <li>Python</li>
            <li>HTML</li>
            <li>CSS</li>
        </ul>
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
            linkedin:"https://br.linkedin.com/in/geovanna-domingos-b31b79190"
        }
    }
}
</script>