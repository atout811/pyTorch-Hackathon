<template>
  <v-container fill-height class="bubble-background">
    <v-row justify="center">
      <v-card tile :loading="loading" width="500">
        <v-card-title> Signup </v-card-title>
        <form @submit.prevent="signup">
          <v-card-text>
            <v-text-field
              v-model="username"
              label="Username"
              hint="john@example.com"
              :disabled="loading"
            ></v-text-field>
            <v-text-field
              v-model="password"
              label="Password"
              type="password"
              :disabled="loading"
            ></v-text-field>
            <v-text-field
              v-model="password_confirm"
              label="Confirm Password"
              type="password"
              :disabled="loading"
            ></v-text-field>
          </v-card-text>
          <v-card-actions>
            <v-btn type="submit" :loading="loading" color="primary" block
              >Signup</v-btn
            >
          </v-card-actions>
        </form>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      password: "",
      password_confirm: "",
      loading: false,
    };
  },
  methods: {
    signup() {
      this.loading = true;
      console.log("signup");
      setTimeout(() => {
        this.loading = false;
      }, 1000);
    },
  },
};
</script>

<style>
</style>