<template>
  <a :href="link" class="card">
    <img :src="image" alt="Project Image" />
    <div class="text-component">
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
    </div>
  </a>
</template>
  
<script>
export default {
  name: 'CardComponent',
  props: {
    image: String,
    title: String,
    description: String,
    link: String,
  },
}
</script>

<style scoped>
.card {
  align-items: start;
  display: flex;
  flex-direction: row;
  border: 1px solid #ccc;
  padding: 16px;
  margin: 16px;
  border-radius: 8px;
  text-align: center;
  background-color: #f9f9f9;
  width: 40%;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.5s ease, box-shadow 0.5s ease;
  text-decoration: none; /* Remove underline from link */
  color: inherit; /* Inherit text color */
}

.card img {
  max-width: 200px;
  max-height: 200px;
  object-fit: cover;
}

.text-component {
  margin-left: 16px;
  text-align: left;
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  background-color: #f0f0f0;
}
@media (max-width: 1170px) {
  .card {
    flex-direction: column;
    align-items: center;
  }

  .card img {
    width: 100%;
    height: auto;
  }

  .text-component {
    margin-left: 0;
    margin-top: 16px;
    text-align: center;
  }
}
@media (max-width: 940px) {
  .card {
    width: 60%;
  }
}

@media (max-width: 480px) {
  .card {
    padding: 8px;
    margin: 8px;
    width: 90%;
  }

  .text-component h3 {
    font-size: 1.2em;
  }

  .text-component p {
    font-size: 1em;
  }
}
</style>