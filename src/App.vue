<template>
 <h1>
 REACTION TIMER
 </h1>
 <button @click="genrate">play</button>
 <br>
 <h3>
 About this game:
 after uh pressed the button after some random time u can see a box down uh have to waitfor that box to come and uh have to press that as fast as uh can.u are ranked based on the time uh pressed after the box pops
 </h3>
 <br>
 <br>
 <br>
 <h3 v-if="xu">
 <h3 v-if="!isplaying">you pressed in {{count}} milliseconds </h3></h3>

 <br>
 <br>
 <br>
 <br>
 <center><HelloWorld v-if="isplaying" :time="time" @teju="xuy"></HelloWorld></center>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return{
      isplaying:false,
      time:null,
      xu:false,
      count:0
    }
  },
  methods: {
     genrate(){
       console.log("hii");
       this.time=2000+(Math.random()*5000);
       this.isplaying=true;
     },
      xuy(tuf){
this.count=tuf;
this.xu=true;
this.isplaying=false;
  }
  }
 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
button{
  color:green;
}
</style>
