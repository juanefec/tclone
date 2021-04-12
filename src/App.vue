<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://animal.mx/wp-content/uploads/2020/10/shrek.jpg"
          transition="scale-transition"
          width="40"
        />
      <v-btn
        v-on:click="goto('counter')"
        target="_blank"
        text
      >
        <span class="mr-2">Counter</span>
      </v-btn>

      <v-btn
        v-on:click="goto('stringer')"
        target="_blank"
        text
      >
        <span class="mr-2">Stringer</span>
      </v-btn>
      
      </div>

      <v-spacer></v-spacer>

      
    </v-app-bar>

    <v-main>
      
      <Counter v-if="showView('counter')"/>
     
      
      <Stringer v-if="showView('stringer')"/>
     
    </v-main>
  </v-app>
</template>

<script>
import Counter from './components/Counter';
import Stringer from './components/Stringer';

export default {
  name: 'App',

  components: {
    Counter,
    Stringer
  },

  data: () => ({
    currentView: "counter",
  }),
  methods: {
    showView(view) {
      return view == this.currentView
    },
    goto(where) {
      this.currentView = where
    }
  }
};
</script>
