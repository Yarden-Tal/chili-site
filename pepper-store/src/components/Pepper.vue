<template>
  <v-card
    class="mx-auto"
    max-width="97vw"
  >
    <v-card-item title="הבנרו צהוב">
      
      <template v-slot:subtitle>
        Yellow Habanero
      </template>
    </v-card-item>

    <v-card-text class="py-0">
      <v-row no-gutters>
        <v-col
          class="text-h3"
        >
         {{ pepperEmojis }}
        </v-col>

        
      </v-row>
    </v-card-text>

    <div class="d-flex py-3 justify-space-between">
      <v-list-item
        density="compact"
        prepend-icon="mdi-check-circle-outline"
        style="color: green"
      >
        <v-list-item-subtitle>{{ "5 פלפלים" }}</v-list-item-subtitle>
      </v-list-item>

      <v-list-item>
        <v-img
      cover
      height="250"
      width="250"
      src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
      ></v-img>

      </v-list-item>
    </div>

    <v-expand-transition>
      <div v-if="expand">
        <div class="py-2">
          <Form />
        </div>
      </div>
    </v-expand-transition>

    <v-divider></v-divider>

    <v-card-actions>
      <v-btn @click="expand = !expand">
        {{ !expand ? 'להזמנה' : 'סגור' }}
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue';
import Form from "../components/Form.vue";

  // DATA
const inStock = ref(true);
const expand = ref(false);
const spiciness = ref(2);
const labels = ref({ 0: 'SU', 1: 'MO', 2: 'TU', 3: 'WED', 4: 'TH', 5: 'FR', 6: 'SA' })
const time = ref(0);
const forecast = ref([
        { day: 'Tuesday', icon: 'mdi-white-balance-sunny', temp: '24\xB0/12\xB0' },
        { day: 'Wednesday', icon: 'mdi-white-balance-sunny', temp: '22\xB0/14\xB0' },
        { day: 'Thursday', icon: 'mdi-cloud', temp: '25\xB0/15\xB0' },
      ]);

      const pepperEmojis = computed(() => {
// COMPUTED
  let peppersString = ""
  if(spiciness.value === 1) peppersString = "🌶️";
  else if(spiciness.value === 2) peppersString = "🌶️🌶️";
  else peppersString = '🌶️🌶️🌶️'
  return peppersString;

})

</script>