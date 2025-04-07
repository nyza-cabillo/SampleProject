<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
</script>

<template>
  <AppLayout>
    <template #content>
      <v-container fluid>
        <v-row>
          <v-col cols="12" md="8" class="bg-surface-light h-screen" v-if="!mobile"></v-col>
          <v-col cols="12" md="4" :class="mobile ? '' : 'pt-16'">
            <v-card
              class="mx-auto"
              prepend-icon="mdi-account-plus"
              subtitle="Registration Form"
              elevation="24"
            >
              <template v-slot:title>
                <span class="font-weight-black">Welcome to Sample Project</span>
              </template>

              <v-card-text class="bg-surface-light pt-4">
                <v-form fast-fail @submit.prevent>
                  <v-text-field label="Email" variant="outlined"></v-text-field>
                  <v-text-field label="First Name" variant="outlined"></v-text-field>
                  <v-text-field label="Last Name" variant="outlined"></v-text-field>

                  <v-text-field label="Password" type="password" variant="outlined"></v-text-field>

                  <v-text-field
                    label="Confirm Password"
                    type="password"
                    variant="outlined"
                  ></v-text-field>

                  <v-btn class="mt-2" type="submit" block prepend-icon="mdi-account-plus"
                    >Register</v-btn
                  >
                </v-form>
                <v-divider class="my-5"></v-divider>
                <h5 class="text-center">
                  Already have account?
                  <RouterLink to="login"><u>Click here to Login!</u></RouterLink>
                </h5>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </template>
  </AppLayout>
</template>
