<template>
  <v-card color="grey darken-3" align="center">
    <v-app-bar color="grey darken-4" flat>
      <v-toolbar-title class="title white--text pl-0 ml-2"
        >Messages</v-toolbar-title
      >
    </v-app-bar>
    <v-list subheader color="grey darken-3" class="pt-4">
      <v-row
        class="pl-2"
        justify="space-around"
        align-content="center"
        v-for="chat in recent"
        :key="chat.id"
      >
        <v-col align-self="center" md="3">
          <v-list-item-avatar>
            <v-img :alt="`${chat.title} avatar`" :src="chat.avatar"> </v-img>
          </v-list-item-avatar>
        </v-col>
        <v-col align-self="center" md="6">
          <v-list-content>
            <v-list-item-title class="mr-5">{{ chat.title }}</v-list-item-title>
          </v-list-content>
        </v-col>
        <v-col align-self="center" md="3">
          <v-icon :color="chat.active ? 'deep-purple accent-4' : 'grey'">
            {{ icons.message }}
          </v-icon>
        </v-col>
      </v-row>
    </v-list>
  </v-card>
</template>

<script>
import * as Icons from "../constants/icons";

export default {
  name: "CardMessages",
  data: () => ({
    icons: {
      message: Icons.ICON_MESSAGE,
    },
    recent: [
      {
        id: 1,
        active: true,
        avatar:
          "https://images.unsplash.com/photo-1539571696357-5a69c17a67c6?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
        title: "Jason Bourne",
      },
      {
        id: 2,
        active: true,
        avatar:
          "https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80",
        title: "Cindy Lauper",
      },
      {
        id: 3,
        avatar:
          "https://images.unsplash.com/photo-1501196354995-cbb51c65aaea?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=751&q=80",
        title: "Mike Wazowsky",
      },
      {
        id: 4,
        avatar:
          "https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
        title: "Lisa Connors",
      },
    ],
  }),
};
</script>

<style>
</style>