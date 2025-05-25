<template>
  <nav
    class="navbar navbar-expand-lg navbar-dark"
    style="
      background-color: #2d64a3;
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
    "
  >
    <div class="container-fluid">
      <!-- Logotipo -->
      <a class="navbar-brand d-flex align-items-center" href="#">
        <img
          src="@/assets/logo.png"
          alt="Logo Ekballo"
          style="max-height: 50px"
          class="me-2"
        />
        <span class="d-none d-sm-inline">Ekballo Consultoria, SU, LDA</span>
      </a>

      <!-- Botão toggler mobile -->
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <!-- Itens de menu -->
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <a class="nav-link" href="#about">Sobre Nós</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#mission">Missão e Visão</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#services">Serviços</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contact">Contato</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#social">Redes Sociais</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup></script>
