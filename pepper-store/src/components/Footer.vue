<template>
    <v-footer class="d-flex flex-column">
      <div class="bg-teal d-flex w-100 align-center px-4 py-2">
        <strong>צרו איתי קשר!</strong>
  
        <v-spacer></v-spacer>
  
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
          :icon="icon"
          variant="plain"
          size="medium"
        ></v-btn>
      </div>
  
      <div class="px-4 py-2 bg-black text-center w-100">
        {{ new Date().getFullYear() }} — <strong>ירדן טל</strong>
      </div>
    </v-footer>
  </template>

<script setup lang="ts">
import { ref } from 'vue';

const icons = ref(['mdi-facebook',
      'mdi-linkedin',
      'mdi-instagram',
      ])
</script>