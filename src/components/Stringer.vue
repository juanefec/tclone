<template>
  <v-container>
    <v-row class="text-center">
      <v-col
        class="mb-4"
        cols="12"
      >
        <h1 class="headline font-weight-bold mb-6">Stringer</h1>
      </v-col>
     
      <v-col
        class="mb-4"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          {{ wierdParagraph }}
        </h2>

        <v-row justify="center">
          <input @keyup.enter="add(text)" v-model="text" type="text">
        </v-row>
      </v-col>

      <v-col
        class="mb-4"
        cols="12"
      >
        <v-row justify="center">
          <v-btn v-on:click="add(text)">Add</v-btn>
        </v-row>
      </v-col>

      
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      wierdParagraph: "",
      text: ""
    }),
    methods: {
      add(a) {
        this.wierdParagraph += " "+a
        this.text = ""
      }
    }
  }
</script>
