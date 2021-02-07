<template>
  <v-navigation-drawer v-model="drawer" app dark color="grey darken-3">
      <v-list-item class="mb-10 mt-10 d-flex justify-center">
        <v-icon x-large>{{ iconDashboard }}</v-icon>
      </v-list-item>
      <v-list>
        <v-list-item-group
          v-model="selectedItem"
          color="green"
        >
          <v-list-item
            v-for="item in items"
            :key="item.id"
            active-class="border"
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              {{ item.text }}
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
  </v-navigation-drawer>
</template>

<script>
import * as Icons from "../constants/icons";

export default {
  data: () => ({
    drawer: null,
    selectedItem: 1,
    iconDashboard: Icons.ICON_DASHBOARD,
    items: [
      { text: "Dashboard", icon: Icons.ICON_DASHBOARD },
      { text: "Projects", icon: Icons.ICON_BRIEFCASE },
      { text: "My Task", icon: Icons.ICON_MENU },
      { text: "Calendar", icon: Icons.ICON_CALENDAR },
      { text: "Tipe Manage", icon: Icons.ICON_CHART },
      { text: "Reports", icon: Icons.ICON_DASHBOARD },
      { text: "Settings", icon: Icons.ICON_SETTINGS },
    ],

  }),
};
</script>

<style scoped>
.border {
  border-right: 5px solid green;
}
</style>