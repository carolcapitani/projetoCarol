<template>
  <nav class="bg-pink-300 text-gray-600 p-4">
    <ul class="flex space-x-4 justify-center">
      <!-- Home com ação de recarga -->
      <li>
        <NuxtLink to="/home" class="hover:underline" @click.prevent="reloadHome">
          Home
        </NuxtLink>
      </li>
      <li><NuxtLink to="/contacts" class="hover:underline">Contatos</NuxtLink></li>
      <li><NuxtLink to="/career" class="hover:underline">Carreira</NuxtLink></li>
      <li><NuxtLink to="/academic" class="hover:underline">Formação Acadêmica</NuxtLink></li>
      <li><NuxtLink to="/personal" class="hover:underline">Vida Pessoal</NuxtLink></li>
    </ul>
  </nav>
</template>

<script setup>
import { useRouter } from 'vue-router';

const router = useRouter();

// Função para navegar para /home e forçar o reload
const reloadHome = () => {
  // Navega para /home, recarregando a página
  router.push('/home').then(() => {
    window.location.reload();
  });
};
</script>
