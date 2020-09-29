<template>
 <div id="app">
 
    <HelloWorld msg="Rx-7" />
    <hr>
    <div class="row">
      <div class="col-6">
   <img src="https://www.drifted.com/wp-content/uploads/2014/02/MadMike_1920x1280.jpg" width="500" height="300" /> 
     
     
        <h1>{{total1}}</h1>
      </div>
      <div class="col-6">
  <img src="https://i.pinimg.com/originals/11/39/38/1139388fb46dbbf1663492857efec811.jpg" width="350" height="300" />
        <h1>{{total2}}</h1>
      </div>
      <div class="col-6">
        <CsButton @cc="sum" />
      </div>
      <div class="col-6">
        <CsButton @cc="sem" />
      </div>
    </div>
    
  </div>
</template>
<script>
import HelloWorld from "./components/HelloWorld.vue";
import CsButton from "./components/CsButton.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    CsButton,
    
  },
  data : function(){
    return {
    total1: 0,
    total2: 0,
   
   } 
  },
  methods: {
  sum(counterValue){
    this.total1 = counterValue
  },
  
  sem(counterValue){
    this.total2 = counterValue
 
  
},
},

};

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ff0bde;
  margin-top: 60px;
  
}
body {

  background-size: 100%;
}
</style>

