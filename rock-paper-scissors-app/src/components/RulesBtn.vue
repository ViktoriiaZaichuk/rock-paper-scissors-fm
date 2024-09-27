<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  label: {
    type: String,
    default: 'Click Me',
  },
});

const emit = defineEmits();

const handleClick = () => {
  emit('clicked');
};
</script>

<template>
    <div>
        <button @click="handleClick">{{ label }}</button>
    </div>
</template>