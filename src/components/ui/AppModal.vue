<template>
  <div
    class="modal-backdrop"
    @click="$emit('close')"
    @keydown.esc="$emit('close')"
  />
  <div class="modal">
    <h3 v-if="title">
      {{ title }}
    </h3>

    <slot />
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    },
  },
  emits: ['close'],
};
</script>

<style scoped>

</style>
