<script setup>
import { ref } from 'vue';

import Choise from './components/Choise.vue';
import Header from './components/Header.vue';
import RulesBtn from './components/RulesBtn.vue';
import RulesModal from './components/RulesModal.vue';

/* Modal */
const isModalVisible = ref(false);

const openModal = () => {
  isModalVisible.value = true; 
};

const closeModal = () => {
  isModalVisible.value = false;
};
</script>

<template>
  <Header />

  <main>
    <Choise />
  </main>

  <RulesBtn label="Rules" @clicked="openModal"/>
  <RulesModal :visible="isModalVisible" @close="closeModal"/>
</template>
