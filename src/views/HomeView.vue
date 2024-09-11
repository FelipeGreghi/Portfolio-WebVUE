<template>
  <div class="home-view">
    <div class="midle-content">
      <h1>I'm Felipe<br>Greghi</h1>
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
/* Definindo animações */
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes slideInLeft {
  from {
    transform: translateX(-100%);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}

@keyframes slideInRight {
  from {
    transform: translateX(100%);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}

/* Aplicando animações */
.home-view {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  width: 100%;
  height: 100%;
  background-color: #f5f5f5;
  animation: fadeIn 1s ease-in-out;
}

.midle-content {
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
  bottom: -120px;
  top: 25%;
  left: 75%;
  transform: translateX(-50%);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.home-view h1 {
  margin: 0 0 1em 0;
  font-size: 5em;
  color: #363E3E;
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
  margin-top: auto;
}

.text-section {
  color: #ffffff;
  max-width: 50%;
  margin-left: 5%;
  animation: slideInLeft 1s ease-in-out;
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

.portfolio-btn:hover {
  background-color: #509295;
}

.portfolio-btn .arrow {
  margin-left: 10px;
  font-size: 1.5rem;
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

/* Media Queries para Responsividade */
@media (max-width: 1200px) {
  .home-view h1 {
    font-size: 4em;
  }

  .midle-content img {
    width: 275px;
    height: 350px;
  }
  .text-section p {
    font-size: 1rem;
  }

  .portfolio-btn {
    padding: 10px 20px;
    font-size: 0.9rem;
  }
}

@media (max-width: 768px) {
  .home-view {
    align-items: center;
  }

  .midle-content {
    flex-direction: column;
    align-items: center;
  }

  .midle-content img {
    display: none;
  }

  .home-view h1 {
    font-size: 4.2em;
    text-align: center;
    margin-left: 0;
  }

  .content {
    flex-direction: column;
    height: auto;
    padding: 2em 1em;
  }

  .text-section {
    max-width: 90%;
    margin-left: 0;
    text-align: center;
  }

  .portfolio-btn {
    margin-top: 20px;
  }
}

@media (max-width: 480px) {
  .home-view h1 {
    font-size: 2.5em;
  }

  .text-section p {
    font-size: 0.9rem;
  }

  .portfolio-btn {
    padding: 8px 15px;
    font-size: 0.8rem;
  }
}
</style>