<template>
  <v-card color="grey darken-2" align="center" class="pb-6">
    <v-app-bar flat color="grey darken-3">
      <v-toolbar-title class="title white--text pl-0 ml-2"
        >Google</v-toolbar-title
      >
    </v-app-bar>
    <v-list color="grey darken-1">
      <v-list-item-group
        v-model="selected1"
        active-class="green--text"
        multiple
      >
        <v-list-item v-for="article in articles" :key="article.id">
          <template v-slot:default="{ active }">
            <v-list-item-content>
              <v-list-item-title>{{ article.title }}</v-list-item-title>
            </v-list-item-content>
            <v-list-item-action>
              <v-spacer></v-spacer>
              <v-list-item-icon>
                <v-btn icon>
                  <v-icon>
                    {{ icons.prev }}
                  </v-icon>
                </v-btn>
                <v-btn v-if="active" icon>
                  <v-icon color="grey lighten-1">
                    {{ icons.play }}
                  </v-icon>
                </v-btn>
                <v-btn v-else icon>
                  <v-icon color="yellow lighten-1">
                    {{ icons.pause }}
                  </v-icon>
                </v-btn>
                <v-btn icon>
                  <v-icon>
                    {{ icons.next }}
                  </v-icon>
                </v-btn>
              </v-list-item-icon>
            </v-list-item-action>
          </template>
          <v-divider
            v-if="article.id < articles.length - 1"
            :key="index"
          ></v-divider>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-card>
</template>

<script>
import * as Icons from "../constants/icons";

export default {
  name: "CardArticles",
  data: () => ({
    icons: {
      prev: Icons.ICON_PREV,
      play: Icons.ICON_PLAY,
      pause: Icons.ICON_PAUSE,
      next: Icons.ICON_NEXT
    },
    articles: [
      { id: 1, title: "01 How to Create a Wireframe?" },
      { id: 2, title: "02 How to Design a Slack Logo?" },
    ],
  })
};
</script>

<style>
</style>