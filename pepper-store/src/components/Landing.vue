<template>
  <v-container class="fill-height">
    <v-responsive class="d-flex align-center text-center fill-height">
      <v-img
        contain
        height="300"
        src="@/assets/logo.svg"
      />

      <div class="text-body-2 font-weight-light mb-n1">ברוכים הבאים</div>

      <h1 class="text-h3 font-weight-bold">לחנות הפלפלים של בת גלים</h1>

      <div class="text-body-2 font-weight-light mb-n1 text-primary">פלפלים חריפים אורגניים וטריים</div>

      <div class="py-14" />

      <v-row class="d-flex align-center justify-center">
        <v-col cols="auto">
          <v-btn
            href="https://www.chilipeppermadness.com/chili-pepper-types/"
            min-width="164"
            rel="noopener noreferrer"
            target="_blank"
            variant="text"
          >
            <v-icon
              icon="mdi-view-dashboard"
              size="large"
              start
            />

            בכללי על פלפלים חריפים
          </v-btn>
        </v-col>

        <v-col cols="auto">
          <v-btn
            color="primary"
            href="/store"
            min-width="228"
            rel="noopener noreferrer"
            size="x-large"
            variant="flat"
          >
            <v-icon
              icon="mdi-speedometer"
              size="large"
              start
            />

            לחנות
          </v-btn>
        </v-col>

        <v-col cols="auto">
          <v-btn
            href="https://github.com/Yarden-Tal"
            min-width="164"
            rel="noopener noreferrer"
            target="_blank"
            variant="text"
          >
            <v-icon
              icon="mdi-github"
              size="large"
              start
            />

          (GitHub) ירדו טל
          </v-btn>
        </v-col>
      </v-row>
    </v-responsive>
  </v-container>
</template>

<script setup lang="ts">
  //
</script>
