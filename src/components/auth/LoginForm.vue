<script setup>
import { ref } from 'vue'

const isPasswordVisible = ref(false)
</script>

<template>
  <v-form fast-fail @submit.prevent>
    <v-text-field label="Email" prepend-inner-icon="mdi-ema"> </v-text-field>

    <v-text-field
      prepend-inner-icon="mdi-lock"
      label="Password"
      :type="isPasswordVisible ? 'text' : 'password'"
      :append-inner-icon="isPasswordVisible ? 'mdi-eye-off' : 'mdi-eye'"
      @click:append-inner="isPasswordVisible = !isPasswordVisible"
    >
    </v-text-field>

    <v-btn class="mt-2" type="submit" block color="deep-red-lighten-1" prepend-icon="pi-sign-in">
      Login
    </v-btn>
  </v-form>
</template>
