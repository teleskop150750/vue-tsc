<script setup lang="ts">
defineOptions({
  name: 'NButton'
})

defineProps<{
  text: string;
}>();

const emit = defineEmits<{
  (e: 'click', event: MouseEvent): void
}>();

function handleCLick(event: MouseEvent) {
  emit('click', event);
}
</script>

<template>
  <button type="button" @click="handleCLick">
    {{ text }}
  </button>
</template>
