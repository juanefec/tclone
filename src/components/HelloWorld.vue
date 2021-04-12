<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{ subtitulo }}</h2>
    <h1>{{ count }}</h1>
    Input: <input v-model="inputCount" type="number">
    <button v-on:click="addCount(inputCount)">Add</button>
    <button v-on:click="subCount(inputCount)">Substract</button>
    
  </div>
</template>


<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      subtitulo: "soy un h2 probablemente",
      count: 0,
      inputCount: 0
    }
  },
  methods: {
    addCount(num) {
      this.count += parseInt(num)
    },
    subCount(num) {
      this.count -= parseInt(num)
    }
  }

}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
