<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>

    <div class="wrapper">
      <HelloWorld msg="BEM-VINDOS" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">Sobre</RouterLink>
      </nav>
    </div>
        <form>
          <h1 id="frase_titulo">CRIAR CADASTRO</h1>
            <input class="input" type="text" name="nome" value="" placeholder="Nome:" />
                <input class="input" type="email" name="email" placeholder="E-mail"/><br>
                <input class="input" type="text" autocomplete="off" maxlength="2" name="estado" placeholder="Sigla do seu Estado"/><br>
                <input class="input" type="tel" id="telefone" autocomplete="off" maxlength="15" name="tel" placeholder="Telefone:EX:(99)9-9999-9999"/><br>
                <input class="input" type="password" name="senha" placeholder="Senha:"/><br>
                <input class="input" type="password" placeholder="Confirmar Senha:">
                <input class="enviar" type = "submit"><br>        
                <p class="comlogin">Já tem cadastro? <a class="comlogin" href="login.html">Clique aqui!</a></p> 
        </form>
  </header>
  <RouterView />
</template>

<style scoped>

form{
    padding: 50px;
    float: left;
    height: 550px;
    width: 550px;
    background-position: relative;
    background-color: black;
    border-radius: 45px 45px 45px 45px;
    font-size:22px;
    margin: 0 auto 0;
    z-index: 999999;
}

h1#frase_titulo{
    color:white;
    font-size: 40px;
    position: relative;
}

.input{
    border-radius: 20px 20px 20px 20px;
    height: 40px;
    width: 475px;
    margin:2px;
    font-size: none;
    padding: 20px;
    
}

.enviar{
    border-radius: 50px 50px 50px 50px;
    height: 40px;
    width: 475px;
    margin: 7px;
    float: center;
}

.comlogin{
    font-size: 18px;
    margin-top: 1px;
    color: white;
    text-decoration: none;
}

header {
  line-height: 1.5;
  max-height: 100vh;
}


nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>