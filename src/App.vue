<script setup lang="ts">
import { ref, onMounted } from "vue";
import Navbar from "./components/Navbar.vue";
import AboutSection from "./components/AboutSection.vue";
import MissionVisionSection from "./components/MissionVisionSection.vue";
import ServicesSection from "./components/ServicesSection.vue";
import ContactSection from "./components/ContactSection.vue";
import SocialSection from "./components/SocialSection.vue";
import FooterSection from "./components/FooterSection.vue";

const showArrow = ref(false);
const lastSection = ref<HTMLElement | null>(null);

function scrollToTop() {
  document.documentElement.scrollTo({ top: 0, behavior: "smooth" });
  document.body.scrollTo({ top: 0, behavior: "smooth" });
}

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      showArrow.value = entries[0].isIntersecting;
    },
    { threshold: 0.5 } // aparece quando 50% da última seção está visível
  );

  if (lastSection.value) {
    observer.observe(lastSection.value);
  }
});
</script>

<template>
  <Navbar />

  <main style="margin-top: 80px">
    <AboutSection />
    <MissionVisionSection />
    <ServicesSection />
    <ContactSection />

    <!-- Última seção observada -->
    <div ref="lastSection">
      <SocialSection />
    </div>

    <FooterSection />
  </main>

  <!-- Seta flutuante para o topo -->
  <div
    v-if="showArrow"
    class="arrow-to-top"
    @click="scrollToTop"
    title="Voltar ao topo"
  >
    <i class="bi bi-arrow-up-circle-fill"></i>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

/* Seta flutuante para o topo */
.arrow-to-top {
  position: fixed;
  bottom: 30px;
  right: 30px;
  width: 60px;
  height: 60px;
  background-color: #28a745; /* verde bonito (Bootstrap green) */
  color: #fff; /* ícone branco */
  border-radius: 50%;
  font-size: 28px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  z-index: 9999;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
  transition: background-color 0.3s, transform 0.3s;
}

.arrow-to-top:hover {
  background-color: #218838; /* verde mais escuro ao passar o mouse */
  transform: scale(1.1);
}

html,
body {
  font-family: "Poppins", sans-serif;
}
</style>
