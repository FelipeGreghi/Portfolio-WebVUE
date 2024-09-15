<template>
  <div class="card">
    <div class="card-header">
      <img class="profile-pic" :src="image" alt="Profile Picture" />
    </div>
    <div class="card-body">
      <blockquote>
        "{{ content }}"
      </blockquote>
      <h3 class="name">{{ name }}</h3>
      <p class="job-title">{{ position }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProfileCard',
  props: {
    name: String,
    position: String,
    content: String,
    image: String,
  },
};
</script>

<style scoped>
.card {
  width: 250px;
  padding: 20px;
  border-radius: 10px;
  background-color: #ffffff;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.card-header {
  margin-bottom: 15px;
}

.profile-pic {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  object-fit: cover;
}

.card-body blockquote {
  font-style: italic;
  color: #666;
  margin: 15px 0;
}

.name {
  font-size: 18px;
  font-weight: bold;
  color: #46babe; 
}

.job-title {
  font-size: 14px;
  color: #999;
}
</style>
