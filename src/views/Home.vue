<template>
  <div class="home">
    <div class="m-5 secondary text-no-wrap rounded-lg">
      <search-bar></search-bar>
    </div>
    <div class="mt-n3">
      <v-container>
        <v-row class="mt-2">
          <v-col cols="12" sm="4">
            <card-progress></card-progress>
          </v-col>
          <v-col cols="12" md="4">
            <card-tasks></card-tasks>
          </v-col>
          <v-col cols="12" md="4">
            <v-card color="grey darken-3" align="center">
              <v-date-picker
                v-model="date2"
                :event-color="(date) => (date[9] % 2 ? 'red' : 'yellow')"
                :events="functionEvents"
                color="grey darken-4"
              ></v-date-picker>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
           <card-communication></card-communication>
          </v-col>
          <v-col cols="12" sm="4" md="4">
            <card-articles></card-articles>
          </v-col>
          <v-col cols="12" sm="4" md="4">
            <card-messages></card-messages>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
import CardArticles from '../components/CardArticles.vue';
import CardCommunication from '../components/CardCommunication.vue';
import CardMessages from '../components/CardMessages.vue';
import CardProgress from '../components/CardProgress.vue';
import CardTasks from '../components/CardTasks.vue';
import SearchBar from '../components/SearchBar.vue';
import * as Icons from "../constants/icons";

export default {
  name: "Home",
  components: {CardProgress, CardTasks, CardCommunication, CardArticles, CardMessages, SearchBar},
  data: () => ({
    arrayEvents: null,
    date2: new Date().toISOString().substr(0, 10),
    selected: [2],
    selected1: [1],
  }),
  mounted() {
    this.arrayEvents = [, , Array(6)].map(() => {
      const day = Math.floor(Math.random() * 31);
      const d = new Date();
      d.setDate(day);
      return d.toISOString().substr(0, 10);
    });
  },
  methods: {
    functionEvents(date) {
      const [, , day] = date.split("-");
      if ([12, 17, 28].includes(parseInt(day, 10))) return true;
      if ([1, 19, 22].includes(parseInt(day, 10))) return ["red", "#00f"];
      return false;
    },
  },
};
</script>
