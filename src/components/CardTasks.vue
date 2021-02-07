<template>
  <v-card color="grey darken-2" align="center">
              <v-app-bar flat color="grey darken-3">
                <v-toolbar-title class="title white--text pl-0 ml-2"
                  >My Tasks(5)</v-toolbar-title
                >
              </v-app-bar>
              <v-list color="grey darken-3" class="mt-4">
                <v-list-item-group
                  v-model="selected"
                  active-class="green--text"
                  multiple
                >
                  <v-list-item v-for="item in items" :key="item.id">
                    <template v-slot:default="{ active }">
                      <v-list-item-content>
                        <v-list-item-title
                          class="white--text"
                          v-text="item.title"
                        ></v-list-item-title>
                      </v-list-item-content>
                      <v-list-item-action>
                        <v-icon v-if="active" color="yellow lighten-1">{{
                          icons.favourite
                        }}</v-icon>
                        <v-icon v-else color="grey lighten-1">{{
                          icons.favouriteOutline
                        }}</v-icon>
                      </v-list-item-action>
                    </template>
                    <v-divider></v-divider>
                  </v-list-item>
                </v-list-item-group>
              </v-list>
            </v-card>
</template>

<script>
import * as Icons from "../constants/icons";

export default {
  name: "CardTasks",
  data: () => ({
    icons: {
      favourite: Icons.ICON_FAVOURITE,
      favouriteOutline: Icons.ICON_FAVOURITE_OUTLINE,
    },
    items: [
      { id: 1, title: "01 Create Wireframe" },
      { id: 2, title: "02 Slack Logo Design" },
      { id: 3, title: "03 Dashboard Design" },
      { id: 4, title: "04 Create Wireframe" },
    ],
  })
}
</script>

<style>

</style>