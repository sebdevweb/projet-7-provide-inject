<script setup>
  import { provide } from 'vue'

  import Button from './components/Button.vue';
  import Sidebar from './components/Sidebar.vue';
import DarkMode from './components/DarkMode.vue';

  provide('darkMode', false)

</script>


<template>
  <div class="layout">
    <main>
      <h1>Article</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum possimus inventore amet incidunt reiciendis cumque, modi quidem odio id sed pariatur natus similique perferendis ea, quia autem temporibus eum harum earum rerum suscipit illo! A eos atque accusamus, nobis provident minus laboriosam exercitationem placeat, repellat ipsa neque!</p>
      <p>
        <Button>Bouton</Button>
      </p>
    </main>
    <aside class="sidebar">
      <DarkMode>
        <Sidebar />
      </DarkMode>
    </aside>
  </div>
</template>


<style lang="scss">
  .layout {
    display: grid;
    grid-template-columns: 1fr 200px;
    .sidebar {
      background-color: #000;
      color: #fff;
      padding: 1rem;
    }
  }
</style>
