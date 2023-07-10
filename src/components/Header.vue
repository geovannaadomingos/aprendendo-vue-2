<template>
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Projetos</a></li>
        <li><a href="#">Contato</a></li>
    </ul>
</template>

<script>
export default{
    name: "Header"
}
</script>

<style scoped>
    ul {
        list-style: none; 
        display: flex;
        padding-bottom: 25px;
        padding-top: 25px;
        margin-bottom: 15px;
    }

    li {
        width: 33.33%;
        text-align: center;
    }

    a{
        color: #0e0d0d;
        text-decoration: none;
        font-size: larger;
        font-weight: bold;
    }
    a:hover{
        color: #7c7b7b
    }
</style>
