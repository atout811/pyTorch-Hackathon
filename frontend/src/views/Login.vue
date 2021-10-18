<template>
  <v-container fill-height class="bubble-background">
    <v-row justify="center">
      <v-card tile :loading="loading" width="500">
        <v-card-title> Login </v-card-title>
        <form @submit.prevent="login">
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
          </v-card-text>
          <v-card-actions>
            <v-btn type="submit" :loading="loading" color="primary" block
              >Login</v-btn
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
      loading: false,
    };
  },
  methods: {
    login() {
      this.loading = true;
      console.log("login");
      setTimeout(() => {
        this.loading = false;
      }, 1000);
    },
  },
};
</script>

<style>
</style>