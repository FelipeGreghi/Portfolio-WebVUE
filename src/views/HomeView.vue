<template>
  <div class="home-view">
    <div class="midle-content">
      <h1>I'm Felipe Greghi</h1>
      <img src="@/assets/photo.png">
    </div>
    
    <div class="content">
      <div class="text-section">
        <p>
          I am a full-stack developer passionate about creating efficient and scalable solutions. With over 3 years of experience in <b>data management</b> and <b>system integration</b>, I have worked on projects connecting diverse technologies, always striving to simplify and optimize complex processes.
        </p>
        <button class="portfolio-btn">
          My Portfolio
          <span class="arrow">→</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style scoped>
/* O contêiner principal ocupa 100% da tela */
.home-view {
  display: flex;
  flex-direction: column;
  align-items: flex-start; /* Alinha os itens à esquerda */
  width: 100%;
  height: 100%;
  background-color: #f5f5f5;
}

.midle-content{
  display: flex;
  flex-direction: row;
  width: 100%;
  align-items: end;
  position: relative;
}

.midle-content img {
  width: 325px;
  height: 400px;
  position: absolute;
  bottom: -120px; /* Ajuste este valor conforme necessário para ultrapassar os limites da div */
  left: 75%; /* Centraliza horizontalmente */
  transform: translateX(-50%); /* Centraliza horizontalmente */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.home-view h1 {
  margin: 0 0 1em 0; /* Margem inferior para separar do conteúdo */
  font-size: 5em; /* Ajuste o tamanho da fonte conforme necessário */
  color: #363E3E; /* Cor do texto */
  margin-top: auto;
  max-width: 40%;
  margin-left: 10%;
  padding-top: 0.5em;
}

.content {
  background-color: #363E3E;
  border-radius: 5em 5em 0 0; 
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 50%;
  padding-bottom: 2.5em;
}

.text-section {
  color: #ffffff;
  max-width: 50%;
  margin-left: 5%;
}

.text-section h1 {
  font-size: 3rem;
  margin-bottom: 20px;
}

.text-section p {
  font-size: 1.2rem;
  line-height: 1.5;
  margin-bottom: 30px;
}

.portfolio-btn {
  background-color: #46BABE;
  border: none;
  padding: 15px 25px;
  border-radius: 5px;
  color: #fff;
  font-size: 1rem;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
}

.portfolio-btn .arrow {
  margin-left: 10px;
  font-size: 1.5rem;
}

.image-section {
  position: relative;
  margin-right: 5%;
}

.profile-img {
  width: 300px;
  height: auto;
  border-radius: 10px;
}

.badge {
  position: absolute;
  bottom: 20px;
  right: -10px;
  background-color: #46BABE;
  color: #fff;
  padding: 10px 15px;
  border-radius: 25px;
}

.badge span {
  font-size: 1rem;
  font-weight: bold;
}
</style>
