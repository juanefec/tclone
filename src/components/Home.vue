<template>
    <v-container>
    <v-row class="text-center">
      <v-col class="mb-4" cols="12">
        <h1 class="headline font-weight-bold mb-6">Home</h1>
        <h1 class="headline font-weight-bold mb-6">{{ welcomeMessage }}</h1>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
    name: "Home",
    data: () => ({ 
        welcomeMessage: "Greeting earthling"
    })
    
}
</script>
