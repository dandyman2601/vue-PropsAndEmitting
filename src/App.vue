<template>
  <div id="app">
    <h1>Vue Calculator (Props and Emitting)</h1>
    <label for="input1">Input 1:</label>
    <input id="input1" type="text" v-model="getInput1">
    <label for="input2">Input 2:</label>
    <input id="input2" type="text" v-model="getInput2">
  
    <Add :getInput1="getInput1" :getInput2="getInput2" @getAddResult="getResult"></Add>
    <Sub :getInput1="getInput1" :getInput2="getInput2" @getSubResult="getResult"></Sub>
    <Mul :getInput1="getInput1" :getInput2="getInput2" @getMulResult="getResult"></Mul>
    <Div :getInput1="getInput1" :getInput2="getInput2" @getDivResult="getResult"></Div>    

    <h2>Result:<p id="result_id">{{result}}</p></h2>
  </div>
</template>

<script>
import Add from './components/Add.vue'
import Sub from './components/Sub.vue'
import Mul from './components/Mul.vue'
import Div from './components/Div.vue'

export default {
  name: 'App',

  data(){
    return{
      getInput1: "",
      getInput2: "",
      result: "",
      
    }
  },

  methods:{
    getResult(data){
     // document.getElementById("result_id").innerHTML = `<span>${result}</span>`
      this.result = data
      console.log("This is the result: "+ data)
    }
  },

  components: {
    Add,
    Sub,
    Mul,
    Div
  }
}
</script>

<style>
#input1, #input2{
  margin: 10px 5px;
}
label{
  margin-left: 10px;
}
input[type=button]{
  font-size: 35px;
  padding: 5px;
  margin: 5px;
  width: 50px;
  
}
</style>
