<template>
  <div id="app">

    <h1> Ma Calculatrice !! </h1>
 <h4> Entrer 2 nombre dans les champ en bas et le resultat saffichera <br>
      ensuite choissisez ci vous voulez le multiplier ou l'additionner etc </h4>
    <form class="champ">
     
      NB1 <input type='number' v-model ='nb1'> </input>
      NB2 <input type='number' v-model = 'nb2'> </input>
      Results <input type="text" v-model="result"> </input>

    </form>

    </br>

    <button v-on:click='add()'> Addition </button>
    <button v-on:click="mul()"> Multiplication </button>
    <button v-on:click="div()"> Division </button>
    <button v-on:click="sous()"> Soustraction </button>

    </br>
    </br>


  </div>
</template>

<script>

export default {
  name: 'app',
  data() {
    return {
      result : 0, 
      nb1 : 0,
      nb2 : 0,
    };
  },

  methods: {

    add() {

    this.result = parseInt(this.nb1) + parseInt(this.nb2); 
      
    },

    mul() {

this.result = this.nb1 * this.nb2;

    },

    div() {

this.result = this.nb1 / this.nb2;

    },

    sous() {

this.result = this.nb1 - this.nb2;

    },

  }
}
  // this.result = this.result + this.result

</script>


<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
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
