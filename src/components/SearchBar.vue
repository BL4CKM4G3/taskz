<template>
  <v-app-bar color="grey darken-3" dark class="rounded-lg pt-2">
    <v-row justify="space-between" align-content="center">
      <v-col align-self="center" md="3">
        <v-text-field
          label="Search"
          :prepend-icon="icons.search"
          color="white"
        ></v-text-field>
      </v-col>
      <v-spacer></v-spacer>
      <v-col align-self="center" md="4">
        <v-row class="pr-2 pb-4" justify="end" align-content="center">
          <v-btn class="mr-1" icon
            ><v-icon>{{ icons.bell }}</v-icon></v-btn
          >
          <v-avatar>
            <v-img src="../assets/profile_photo.jpg" alt="john"></v-img>
          </v-avatar>
        </v-row>
      </v-col>
    </v-row>
  </v-app-bar>
</template>

<script>
import * as Icons from "../constants/icons";

export default {
  name: "SearchBar",
  data: () => ({
    icons: {
      search: Icons.ICON_SEARCH,
      bell: Icons.ICON_BELL
    }
  })
};
</script>

<style>
</style>