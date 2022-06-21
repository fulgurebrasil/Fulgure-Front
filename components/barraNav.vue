<template>
    <nav>
        <ul>
            <NuxtLink to="/tela-jogar"><li><a>Home</a></li></NuxtLink>
            <li><a>Sobre nós</a></li>
            <li><a>Entrar em contato</a></li>
            <li><a>Reportar problema</a></li>
        </ul>
    </nav>
</template>

<script>
export default {

}
</script>

<style>
nav {
    background-color: white;
    width: 100%;
    height: 50px;
    left: 0;
    z-index: 4;
    padding-top: 10px;
}

nav ul li {
    padding: 10px;
    height: 100%;
    color: black;
    text-decoration: none;
    cursor: pointer;
    display: inline;
    margin-right: 30px;
    font-size: 16px;
    transition: 1s;
}


nav ul li:hover {
    height: 105%;
    font-size: 20px;
    background-color: black;
    color: white;
}
</style>