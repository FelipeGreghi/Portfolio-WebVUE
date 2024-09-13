<template>
  <div class="testimonial">
    <div class="header">
      <img src="" alt="" />
      <p>{{ name }} • {{ position }} •{{ date }}</p>
    </div>
    <p>
      "{{ content }}" <b> - {{ name }}</b>
    </p>
  </div>
</template>
<script>
export default {
  name: 'TestimonialComponent',
  props: {
    name: String,
    position: String,
    date: String,
    content: String,
  },
}
</script>
<style scoped>
</style>