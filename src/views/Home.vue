<template>
  <v-container class="pa-10">
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to Airports
        </h1>
        <h4 class="text-center ma-10">
          Center aligned text on all viewport sizes.
        </h4>
      </v-col>

      <v-col class="mb-5" cols="12">
        <v-row justify="center">
          <router-link to="/airports">
            <v-btn large>see all airports</v-btn>
          </router-link>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  // components: {
  //   HelloWorld,
  // },
};
</script>
