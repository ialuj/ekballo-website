<template>
  <section id="testemunhos" class="section bg-white">
    <div class="container text-center">
      <h2 class="section-title">O que dizem sobre nós</h2>
      <div class="testimonials-wrapper">
        <div
          v-for="(testimonial, index) in testimonials"
          :key="index"
          class="testimonial-card"
        >
          <p class="quote">"{{ testimonial.message }}"</p>
          <strong>— {{ testimonial.author }}</strong>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    message:
      "A Ekballo cuidou de todo processo de Reserva de nome ao Licenciamento da nossa Empresa, com seriedade e agilidade. Recomendamos.",
    author: "José Julai, Phanda Tech Solutions, SU, LDA.",
  },
];
</script>

<style scoped>
.section {
  padding: 60px 20px;
}
.bg-white {
  background-color: #fff;
}
.section-title {
  font-size: 28px;
  margin-bottom: 40px;
}
.testimonials-wrapper {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}
.testimonial-card {
  flex: 1 1 280px;
  background-color: #f1f1f1;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.05);
}
.quote {
  font-style: italic;
  margin-bottom: 10px;
}
</style>
