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
          position: 'Analista de dados',
          content:
            'Felipe is one of the best professionals I’ve worked with. He delivers projects on time with excellence and an indispensable attention to detail.',
          image: require('@/assets/testimonialsPhotos/profileImageGJ.jpg'),
        },
        {
          id: 2,
          name: 'Coming Soon',
          position: 'Coming Soon',
          content: 'More testimonials coming soon.',
          image: require('@/assets/Comingsoon.png'),
        },
        {
          id: 3,
          name: 'Coming Soon',
          position: 'Coming Soon',
          content: 'More testimonials coming soon.',
          image: require('@/assets/Comingsoon.png'),
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