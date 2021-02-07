<template>
  <v-app>
    <sidebar></sidebar>
    <v-main class="grey darken-4">
      <v-container>
        <transition name="fade">
          <router-view></router-view>
        </transition>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Sidebar from "./components/Sidebar.vue"


export default {
  name: 'App',

  components: {
    Sidebar
  },

  data: () => ({
    //
  }),
};
</script>

<style lang="scss">
html::-webkit-scrollbar {
  width: 7px;
  background: #646464;
}

html::-webkit-scrollbar-thumb {
  width: 7px;
  background: #373737;
}
</style>