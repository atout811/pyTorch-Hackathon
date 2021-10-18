<template>
  <v-container>
    <v-row>
      <v-col
        v-for="(char, i) in results"
        :key="i"
        class="d-flex child-flex"
        cols="4"
      >
        <v-card class="mx-auto" max-width="344">
          <v-img :src="char.image" height="200px"></v-img>

          <v-card-title>{{ char.name }}</v-card-title>

          <v-card-subtitle
            >{{ char.gender }} | {{ char.species }} |
            {{ char.origin.name }}</v-card-subtitle
          >
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      results: [],
    };
  },
  created() {
    this.$axios
      .get("https://rickandmortyapi.com/api/character")
      .then(({ data }) => {
        this.results = data.results;
      });
  },
};
</script>
