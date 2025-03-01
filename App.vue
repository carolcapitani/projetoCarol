<script setup>
import Navigation from "@/components/Navigation.vue";
import Footer from "@/components/Footer.vue";
import 'font-awesome/css/font-awesome.min.css';

console.log("🚀 App.vue carregado!");
</script>

<template>
  <div>
    <h1 class="text-3xl font-bold text-center text-pink-500">Capitani.dev</h1>
    <Navigation />
    <NuxtPage />
    <Footer />
  </div>
</template>
