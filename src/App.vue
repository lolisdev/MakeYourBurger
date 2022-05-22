<template>
  <Navbar :logo="logo_src" :alt="app_name" />
  <router-view/>
  <Footer />
</template>

<script>
/* MELHORIAS:
  - Verificar o problema para o segundo pedido simultâneo;
  - Realizar validações de seleções inexitentes "Selecione...";
  - Melhorar layout da tabela de pedidos.
  - Corrigir link de "Fazer Pedidos" na tela de "Pedidos";
*/

import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
export default {
  components: {
    Navbar,
    Footer
  },
  data(){
    return {
      logo_src: "/img/logo.png",
      app_name: "Make Your Burger"
    }
  }
}
</script>

<style>
  * {
    font-family: Helvetica;
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  .main-container {
    margin: 50px;
    min-height: 600px;
  }

  h1 {
    text-align: center;
    font-size: 42px;
    margin-bottom: 30px;
    color: #222;
  }
</style>
