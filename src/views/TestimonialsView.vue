<template>
  <div class="testimonials-section">
    <h4 class="subheading">What My Clients Say</h4>
  </div>
  <div class="testimonials">
    <ProfileCard
      v-for="testimonial in testimonials"
      :key="testimonial.id"
      :name="testimonial.name"
      :position="testimonial.position"
      :content="testimonial.content"
      :image="testimonial.image"
    />
  </div>
</template>

<script>
import ProfileCard from '../components/Testimonial.vue';

export default {
  name: 'TestimonialsView',
  components: {
    ProfileCard,
  },
  data() {
    return {
      testimonials: [
        {
          id: 1,
          name: 'João Silva',
          position: 'Desenvolvedor Front-end',
          content: 'Este produto é incrível! Mudou completamente a forma como trabalho.',
          image: require('@/assets/Comingsoon.png'),
        },
        {
          id: 2,
          name: 'Maria Oliveira',
          position: 'Gerente de Projetos',
          content: 'A equipe é extremamente profissional e o suporte é excelente.',
          image: require('@/assets/Comingsoon.png'),
        },
        {
          id: 3,
          name: 'Carlos Pereira',
          position: 'Designer Gráfico',
          content: 'As funcionalidades são exatamente o que eu precisava. Recomendo!',
          image: require('@/assets/Comingsoon.png'),
        },
        {
          id: 4,
          name: 'Carlos Pereira',
          position: 'Designer Gráfico',
          content: 'As funcionalidades são exatamente o que eu precisava. Recomendo!',
          image: require('@/assets/Comingsoon.png'),
        },
      ],
    };
  },
};
</script>

<style scoped>

.testimonials {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 16px;
  margin-bottom: 40px;
  width: 80%;
}

.testimonials-section {
  text-align: center;
  padding: 40px 20px;
}

.subheading {
  font-size: 14px;
  color: #666;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-bottom: 10px;
}

</style>