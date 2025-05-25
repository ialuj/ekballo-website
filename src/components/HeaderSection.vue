<template>
  <header class="text-white py-4" style="background-color: #2d64a3">
    <div class="container">
      <div class="row align-items-center">
        <!-- Logotipo à esquerda -->
        <div class="col-md-2 col-12 text-center text-md-start mb-3 mb-md-0">
          <LogoSection />
        </div>

        <!-- Título e slogan centralizados -->
        <div class="col-md-10 col-12 d-flex flex-column align-items-center">
          <h1 class="mb-2 text-center">Ekballo Consultoria, SU, LDA</h1>
          <p class="lead mb-0 text-center">
            Soluções confiáveis para o seu crescimento
          </p>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import LogoSection from "../components/LogoSection.vue";
</script>
