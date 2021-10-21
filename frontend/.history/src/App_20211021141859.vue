<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>
      <v-btn to="/chatbot" text>
        <v-text>Chatbot</v-text>
        <v-icon>mdi-login</v-icon>
      </v-btn>
      <v-btn to="/login" text>
        <v-text>Login</v-text>
        <v-icon>mdi-login</v-icon>
      </v-btn>
      <v-btn to="/signup" text>
        <v-text>Signup</v-text>
        <v-icon>mdi-pencil</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main class="bubble">
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
<style>
.bubble::before {
  background-color: var(--v-primary-base);
  clip-path: circle(80% at 90% 120%);
  width: 100%;
  height: 100%;
  content: "";
  position: absolute;
  box-sizing: none;
  top: 0;
  left: 0;
}
</style>