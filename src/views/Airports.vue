<template>
  <v-card class="pa-5">
    <v-card-title>
      Airports
      <v-spacer></v-spacer>
      <router-link to="/newairport">
        <v-btn>+ Add new airport</v-btn>
      </router-link>
      <v-spacer></v-spacer>
      <v-text-field
        v-model="search"
        append-icon="mdi-magnify"
        label="Search"
        single-line
        hide-details
      ></v-text-field>
    </v-card-title>
    <v-data-table
      :headers="headers"
      :items="airports"
      :items-per-page="10"
      :search="search"
      class="elevation-5"
      fixed-header
      loading
      loading-text="Loading... Please wait"
    ></v-data-table>
  </v-card>
</template>
<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

import { db } from "../db";
export default {
  name: "Airports",
  // components: {
  //   Table,
  // },
  data() {
    return {
      search: "",
      headers: [
        {
          text: "Name",
          align: "start",
          // sortable: false,
          value: "name",
        },
        { text: "City", value: "city" },
        { text: "Country", value: "country" },
        { text: "IATA", value: "iata" },
        { text: "ICAO", value: "icao" },
        { text: "", value: "" },
      ],
      airports: db,
    };
  },
};
</script>
<style scoped>
.airports {
  width: 100%;
  height: 100vh;
}
</style>
