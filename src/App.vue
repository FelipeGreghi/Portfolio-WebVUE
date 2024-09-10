<template>
  <div class="app-layout">
    <Navbar />
    <div class="main-content">
      <router-view />
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Footer
  }
}
</script>

<style>
/* Configuração global do body */
body {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
  background-color: #f5f5f5;
  display: flex;
  flex-direction: column;
  min-height: 100vh; /* Garante que o body ocupe toda a altura da tela */
}

.app-layout {
  display: flex;
  flex-direction: column;
  height: 100vh;
}

.main-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex-grow: 1; /* Faz o main-content crescer para preencher o espaço restante */
  width: 100%;
}
</style>