<template>
  <div class="portfolio">
    <CardComponent
      v-for="project in projects"
      :key="project.id"
      :image="project.image"
      :title="project.title"
      :description="project.description"
      :link="project.link"
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
          image: require('@/assets/Comingsoon.png'),
          title: 'Coming soon',
          description:
            'Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon',
          link: 'https://www.google.com',
        },
        {
          id: 2,
          image: require('@/assets/Comingsoon.png'),
          title: 'Coming soon',
          description:
            'Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon',
          link: 'https://www.google.com',
        },
        {
          id: 3,
          image: require('@/assets/Comingsoon.png'),
          title: 'Coming soon',
          description:
            'Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon Coming soon',
          link: 'https://www.google.com',
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