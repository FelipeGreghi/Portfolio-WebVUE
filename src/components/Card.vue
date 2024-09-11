<template>
  <div class="card">
    <img :src="image" alt="Project Image" />
    <div class="text-component">
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
    </div>
  </div>
</template>
  
<script>
export default {
  name: 'CardComponent',
  props: {
    image: String,
    title: String,
    description: String,
  },
}
</script>

<style scoped>
.card {
  justify-content: center;
  align-items: center;
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
}
</style>