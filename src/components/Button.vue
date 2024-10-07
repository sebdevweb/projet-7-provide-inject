<template>
  <button class="btn">Bouton</button>
</template>


<script setup>
  import { computed, inject } from 'vue'

  const darkMode = inject('darkMode')
  console.log(darkMode);
  

  const props = defineProps({
    dark: Boolean
  })

  const classes = computed(() => ({
    btn: true,
    dark: props.dark || darkMode,
  }))

</script>


<style lang="scss">
  .btn {
    color: #fff;
    background-color: #000;
    border: 1px solid #ddd;
    padding: .5rem 1rem;
    font: inherit;
    &.dark {
      color: #000;
      background-color: #fff;
    }
  }
</style>