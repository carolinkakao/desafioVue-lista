<template>
  <div id="app">
    <label>Ingresar Pokemones</label>
    <input v-model="pokemon" type="text">
    <button @click="ingresarPokemon()">Ingresar Pokemon</button>
      <ol>
        <li v-for="(pokemon,index) in pokemones" :key="index">
          {{pokemon}}
        </li>
      </ol>
  </div>
</template>

<script>
//import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
data() {
  return {
  pokemones:["Mew","Ditto", "Dragonite","Moltres","Pikachu"],
  pokemon:"",
  };
},
methods:{
  async getData(){
   },
   ingresarPokemon(){
     if(this.pokemon === "")return;
     this.pokemones.push(this.pokemon);
     this.pokemon="";
   }

},
  
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}
li{
  position:relative;
  top:5rem;
  left: 2rem;
}
label{
  margin:3rem;
}
button{
  margin: 2rem;
}

</style>
