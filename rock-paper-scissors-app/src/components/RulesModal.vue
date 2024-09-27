<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  visible: {
    type: Boolean,
    required: true,
  },
});

const emit = defineEmits();

const closeModal = () => {
  emit('close');
};
</script>

<template>
    <div  v-if="visible">
        <img src="../assets/images/image-rules.svg" alt="">
        <span class="close" @click="closeModal">&times;</span>
    </div>
</template>