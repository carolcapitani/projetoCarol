<template>
  <div class="p-10">
    <h1 class="text-4xl font-bold text-pink-500">Meus Contatos</h1>
    
    <div class="flex mt-4">
      <img
        src="/images/carol1.jpg" 
        alt="Carol"
        class="w-25 h-44 rounded-full border-4"
      />
    </div>

  
    <div class="mt-6 flex space-x-8">
      <button @click="openModal('whatsapp')" class="text-4xl">
        <img
          src="/images/whatsapp.png"
          alt="WhatsApp"
          class="w-12 h-12 hover:opacity-80"
        />
      </button>
      <button @click="openModal('email')" class="text-4xl">
        <img
          src="/images/email.png"
          alt="Email"
          class="w-12 h-12 hover:opacity-80"
        />
      </button>
      <button @click="openModal('linkedin')" class="text-4xl">
        <img
          src="/images/linkedin.png"
          alt="LinkedIn"
          class="w-12 h-12 hover:opacity-80"
        />
      </button>
      <button @click="openModal('github')" class="text-4xl">
        <img
          src="/images/github.png"
          alt="GitHub"
          class="w-12 h-12 hover:opacity-80"
        />
      </button>
    </div>

    <div
      v-if="isModalOpen"
      class="fixed inset-0 bg-gray-800 bg-opacity-50 flex items-center justify-center z-50"
    >
      <div class="bg-white p-8 rounded-lg w-1/3">
        <h2 class="text-2xl font-semibold text-gray-800 mb-4">
          Informações de {{ modalType }}
        </h2>

        <div class="mb-4">
          <p v-if="modalType === 'whatsapp'" class="text-lg">
            WhatsApp: <strong>+55 11 971840910</strong>
          </p>
          <p v-if="modalType === 'email'" class="text-lg">
            E-mail: <strong>carolcmc.1999@gmail.com</strong>
          </p>
          <p v-if="modalType === 'linkedin'" class="text-lg">
            LinkedIn:
            <strong>
              <a
                href="https://www.linkedin.com/in/carolina-capitani-b91b4b185/"
                target="_blank"
                class="text-blue-600"
                >https://www.linkedin.com/in/carolina-capitani-b91b4b185/</a
              >
            </strong>
          </p>
          <p v-if="modalType === 'github'" class="text-lg">
            GitHub:
            <strong>
              <a
                href="https://github.com/carolcapitani"
                target="_blank"
                class="text-blue-600"
                >https://github.com/carolcapitani</a
              >
            </strong>
          </p>
        </div>

        <div class="flex justify-end space-x-4">
          <button
            @click="closeModal"
            type="button"
            class="px-4 py-2 bg-gray-300 text-white rounded hover:bg-gray-400"
          >
            Fechar
          </button>
        </div>
        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isModalOpen: false,
      modalType: "",
    };
  },
  methods: {
    openModal(type) {
      this.modalType = type;
      this.isModalOpen = true;
    },
    closeModal() {
      this.isModalOpen = false;
    },
  },
};
</script>

<style scoped>
button img {
  transition: transform 0.3s;
}

button:hover img {
  transform: scale(1.1);
}

button {
  border-radius: 50%;
  border: 2px solid transparent;
}

button:hover {
  border: 2px solid #ec4899;
}
</style>
