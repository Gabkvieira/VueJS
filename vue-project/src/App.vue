<script setup>
const nome = "Gabriel Vieira";
const meuObj = {
  nome:"Gabriel",
  filmeFavorito: "Rocky"
}

function dizOla() {
  return `${nome} diz oi`;
}

const enderecoDaImagemDoBatman = "https://cdn1.epicgames.com/undefined/offer/batman-arkham-knight_promo-2048x1152-ed2be22b3f24f446534b90b122ed560d.jpg";
const imagemSuperman = "https://segredosdomundo.r7.com/wp-content/uploads/2020/07/superman-historia-poderes-fraquezas-e-curiosidades.jpg";

const botaoEstaDesabilitado = false;

const gostaDoBatman = false;
const gostaDoSuperman = true;

const estaAutorizado = true;

</script>


<template>
  <h1>{{ dizOla("Paula") }}</h1>
  <img v-if="gostaDoBatman" :src="enderecoDaImagemDoBatman" alt="">
  <img v-else-if="gostaDoSuperman" :src="imagemSuperman" alt="">
  <h2 v-else>Não gosta de heróis da DC</h2>

  <h1 v-if="estaAutorizado">Bem-vindo!</h1>
  <h1 v-else>Não possui acesso</h1>

  <button :disabled="botaoEstaDesabilitado">Enviar mensagem</button>
</template>

<style scoped>

img {
  max-width: 200px;
}

</style>
