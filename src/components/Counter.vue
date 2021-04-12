<template>
  <v-container>
    <v-row class="text-center">
      <v-col
        class="mb-4"
        cols="12"
      >
        <h1 class="headline font-weight-bold mb-6">Counter</h1>
      </v-col>
     
      <v-col
        class="mb-4"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          {{ count }}
        </h2>

        <v-row justify="center">
          <input v-model="amount" type="number">
        </v-row>
      </v-col>

      <v-col
        class="mb-4"
        cols="12"
      >
        <v-row justify="center">
          <v-btn v-on:click="add(amount)">Add</v-btn>
          <v-btn v-on:click="sub(amount)">Sub</v-btn>
        </v-row>
      </v-col>

      
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      count: 0,
      amount: 0
    }),
    methods: {
      add(num) {
        this.count += parseInt(num)
      },
      sub(num) {
        this.count -= parseInt(num)
      }
    }
  }
</script>
