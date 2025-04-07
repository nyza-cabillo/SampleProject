<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
</script>

<template>
  <AppLayout>
    <template #content>
      <v-container fluid>
        <v-row>
          <v-col cols="12" md="8" class="bg-surface-light h-screen" v-if="!mobile">
            <v-img src="img/bg.jpg"></v-img>
          </v-col>
          <v-col cols="12" md="4" :class="mobile ? '' : 'pt-16'">
            <v-card class="mx-auto" elevation="24">
              <v-card-title class="text-center">
                <v-img
                  class="mx-auto"
                  src="/img/cacao.jpg"
                  height="100"
                  width="100"
                  cover
                  rounded="pill"
                ></v-img>
                <h3 class="font-weight-black text-center">Cacao Disease Classification</h3>
                <p class="mb-5">Login Form</p>
              </v-card-title>

              <v-card-text class="bg-surface-light pt-4">
                <v-form fast-fail @submit.prevent>
                  <v-text-field label="Email" variant="outlined"></v-text-field>

                  <v-text-field label="Password" type="password" variant="outlined"></v-text-field>

                  <v-text-field label="Role" type="text" variant="outlined"></v-text-field>

                  <v-btn class="mt-2" type="submit" block prepend-icon="mdi-login">Login</v-btn>
                </v-form>

                <v-divider class="my-5"></v-divider>
                <h5 class="text-center">
                  Don't have account?
                  <RouterLink to="register"><u>Click here to Register!</u></RouterLink>
                </h5>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </template>
  </AppLayout>
</template>
