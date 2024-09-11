<template>
  <div class="portfolio">
    <CardComponent
      v-for="project in projects"
      :key="project.id"
      :image="project.image"
      :title="project.title"
      :description="project.description"
    />
  </div>
</template>
  
  <script>
import CardComponent from '../components/Card.vue'

export default {
  name: 'PortfolioView',
  components: {
    CardComponent,
  },
  data() {
    return {
      projects: [
        {
          id: 1,
          image: 'Coming soon.png',
          title: 'Coming soon',
          description: 'Coming soon',
        },
        {
          id: 2,
          image: 'Coming soon.png',
          title: 'Coming soon',
          description: 'Coming soon',
        },
      ],
    }
  },
}
</script>
  
  <style scoped>
.portfolio {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 16px;
  width: 80%;
}
</style>