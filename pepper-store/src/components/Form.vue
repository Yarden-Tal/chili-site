<template>
    <v-sheet width="300" class="ml-auto">
      <v-form fast-fail @submit.prevent>
        <v-text-field
          v-model="firstName"
          label="First name"
          :rules="firstNameRules"
        ></v-text-field>
  
        <v-text-field
          v-model="lastName"
          label="Last name"
          :rules="lastNameRules"
        ></v-text-field>
  
        <v-btn type="submit" block class="mt-2">Submit</v-btn>
      </v-form>
    </v-sheet>
  </template>

<script lang="ts">
  export default {
    data: () => ({
      firstName: '',
      firstNameRules: [
(        value: string | any[]) => {
          if (value?.length > 3) return true

          return 'First name must be at least 3 characters.'
        },
      ],
      lastName: '123',
      lastNameRules: [
(        value: string) => {
          if (/[^0-9]/.test(value)) return true

          return 'Last name can not contain digits.'
        },
      ],
    }),
  }
</script>