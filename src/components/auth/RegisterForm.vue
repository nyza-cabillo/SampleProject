<script setup>
import { ref } from 'vue'

const isPasswordVisible = ref(false)
const isPasswordConfirmvisible = ref(false)
</script>

<template>
  <v-form fast-fail @submit.prevent>
    <v-row>
      <v-col cols="12" md="6">
        <v-text-field label="firstname"></v-text-field>
      </v-col>

      <v-col cols="12" md="6">
        <v-text-field label="lasttname"></v-text-field>
      </v-col>

      <v-col cols="12">
        <v-text-field label="Email" prepend-inner-icon="mdi-email"></v-text-field>
      </v-col>

      <v-col cols="12" md="6">
        <v-text-field
          prepend-inner-icon="mdi-lock"
          label="Password"
          :type="isPasswordVisible ? 'text' : 'password'"
          :append-inner-icon="isPasswordVisible ? 'mdi-eye-off' : 'mdi-eye'"
          @click:append-inner="isPasswordVisible = !isPasswordVisible"
        >
        </v-text-field>
      </v-col>

      <v-col cols="12" md="6">
        <v-text-field
          prepend-inner-icon="mdi-lock"
          label="Password"
          :type="isPasswordConfirmvisible ? 'text' : 'password'"
          :append-inner-icon="isPasswordConfirmvisible ? 'mdi-eye-off' : 'mdi-eye'"
          @click:append-inner="isPasswordConfirmvisible = !isPasswordConfirmvisible"
        >
        </v-text-field>
      </v-col>
    </v-row>

    <v-btn class="mt-2" type="submit" block color="deep-red-lighten-1"> Register </v-btn>
  </v-form>
</template>
