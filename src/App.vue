<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://animal.mx/wp-content/uploads/2020/10/shrek.jpg"
          transition="scale-transition"
          width="40"
        />

        <template>
          <div id="app">
            <MenuDropdown v-model="currentView" :items="items" color="deep-purple accent-4" text="Menu"/>
          </div>
        </template>
      </div>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <Home v-if="showView('Home')" />

      <Counter v-if="showView('Counter')" />

      <Stringer v-if="showView('Stringer')" />
    </v-main>
  </v-app>
</template>

<script>
import Counter from "./components/Counter";
import Stringer from "./components/Stringer";
import MenuDropdown from "./components/menu-dropdown/MenuDropdown.vue"
import Home from "./components/Home";

export default {
  name: "App",
  components: {
    Counter,
    Stringer,
    MenuDropdown,
    Home
  },
  data: () => ({
    currentView: "Home",
    items: [
      "Home",
      "Counter",
      "Stringer"
    ]
  }),
  methods: {
    showView(view) {
      return view == this.currentView;
    }
  },
};
</script>
