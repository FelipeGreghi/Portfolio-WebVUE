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
import ProfileCard from '../components/Testimonial.vue'

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
          name: 'Gabriel João',
          position: 'Analista de Dados - Krolik',
          content:
            'Felipe is one of the best professionals I’ve worked with. He delivers projects on time with excellence and an indispensable attention to detail.',
          image: require('@/assets/testimonialsPhotos/profileImageGJ.jpg'),
        },
        {
          id: 2,
          name: 'Fabio Bogo',
          position: 'Gerente Comercial - Cubus Soluções',
          content:
            'Felipe is a well-rounded developer in every aspect. An excellent professional with great communication skills, he excels at handling clients and effortlessly manages an entire project lifecycle, from initiation to development and final delivery.',
          image: require('@/assets/testimonialsPhotos/profileImageFB.jpg'),
        },
        {
          id: 3,
          name: 'Julia da Rosa',
          position: 'Project Manager - Cubus Soluções',
          content:
            'Felipe Greghi is a talented programmer with solid skills in algorithms and software development. He excels in solving complex problems and has strong communication skills, enhancing teamwork and idea exchange. With a constant focus on learning and improvement, Felipe combines technical expertise with clear, efficient communication, making him a promising professional in technology.',
          image: require('@/assets/testimonialsPhotos/profileImageJR.jpg'),
        },
      ],
    }
  },
}
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