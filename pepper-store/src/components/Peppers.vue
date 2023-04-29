<template>
  <v-card
    class="mx-auto"
  >
    <v-list>
      <Pepper/>
    </v-list>
  </v-card>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import Pepper from "./Pepper.vue";

  const peppers = ref([
    
  ]);
</script>
