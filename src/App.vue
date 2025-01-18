<script setup>
import Header from "./components/HeaderView.vue";
import Footer from "./components/FooterView.vue";
import Modal from "./components/ModalView.vue";
import { store } from "./store/index.js";
</script>

<template>
  <div class="main-wrapper">
    <Header @toggleModal="store.toggleModal(true)" />

    <main class="main">
      <RouterView></RouterView>
    </main>

    <Modal :isOpen="store.isOpen" @toggleModal="store.toggleModal(false)" />
    <Footer />
  </div>
</template>

<style scoped></style>
