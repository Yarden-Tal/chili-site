<template>
  <v-app>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script setup lang="ts">
    import Landing from '@/components/Landing.vue';
</script>

<style>
  * {
    direction: rtl;
  }
</style>