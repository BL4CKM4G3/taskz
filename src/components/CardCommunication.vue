<template>
  <v-card elevation="10" color="grey-darken-3">
    <v-app-bar flat color="grey darken-4">
      <v-avatar size="45" color="grey darken-2">
        <v-img
          src="https://cdn.mos.cms.futurecdn.net/SDDw7CnuoUGax6x9mTo7dd.jpg"
        >
        </v-img>
      </v-avatar>
      <v-toolbar-title class="title white--text pl-0 ml-2"
        >Slack</v-toolbar-title
      >
      <v-spacer></v-spacer>
      <v-btn color="white" class="mr-1" outlined icon small>
        <v-icon color="yellow">
          {{ icons.favourite }}
        </v-icon>
      </v-btn>
      <v-btn color="white" class="ml-1" outlined icon small>
        <v-icon>
          {{ icons.dots }}
        </v-icon>
      </v-btn>
    </v-app-bar>
    <v-app-bar flat color="grey darken-4">
      <v-btn color="green darken-2" class="white--text" small>Completed</v-btn>
      <v-spacer></v-spacer>
      <v-btn color="green" outlined small>Medium</v-btn>
    </v-app-bar>
    <v-app-bar flat class="mt-n4 pl-2" color="grey darken-4">
      <p class="title white--text">Task Done: 30/30</p>
    </v-app-bar>
    <v-app-bar flat class="mt-n4" color="grey darken-3">
      <v-progress-linear
        class="mb-10"
        color="yellow"
        height="6"
        indeterminate
      ></v-progress-linear>
    </v-app-bar>
    <v-app-bar flat class="mt-n10" color="grey darken-4">
      <v-btn color="green" small class="mr-2" text click>IOS APP</v-btn>
      <v-btn color="blue" small text click>UI/UX</v-btn>
    </v-app-bar>
    <v-app-bar flat color="grey darken-4" class="mb-4 pl-4">
      <v-avatar class="ml-n3" size="30">
        <v-img src="https://cdn.vuetifyjs.com/images/lists/1.jpg"></v-img>
      </v-avatar>
      <v-avatar class="ml-n3" size="30">
        <v-img src="https://cdn.vuetifyjs.com/images/lists/2.jpg"></v-img>
      </v-avatar>
      <v-avatar class="ml-n3" size="30">
        <v-img src="https://cdn.vuetifyjs.com/images/lists/3.jpg"></v-img>
      </v-avatar>
      <v-avatar class="ml-n3" size="30">
        <v-img src="https://cdn.vuetifyjs.com/images/lists/4.jpg"></v-img>
      </v-avatar>
      <v-avatar color="grey darken-2" class="ml-n3" size="30"> +5 </v-avatar>
    </v-app-bar>
    <v-app-bar flat color="grey darken-4" class="mt-n8">
      <v-btn color="red darken-2" small text> Due Date: 28 March </v-btn>
    </v-app-bar>
  </v-card>
</template>

<script>
import * as Icons from "../constants/icons";

export default {
  name: "CardCommunication",
  data: () => ({
    icons: {
      dots: Icons.ICON_DOTS,
      favourite: Icons.ICON_FAVOURITE
    }
  })
};
</script>

<style>
</style>