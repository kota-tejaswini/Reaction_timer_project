<template>
<div @click="gen" v-if="boo" >
<center >
Click as fast as you can</center>
</div>
</template>

<script>
export default {
 
  props: ["time"],
  data(){
    return{
      se:null,
      arc:0,
      boo:false
    }
  },
  mounted(){
    console.log(this.time);
    var v=this;
           setTimeout(
           function(){ v.start();}
           ,this.time);
  },
  updated(){
     console.log(this.time);
    var v=this;
           setTimeout(
           function(){ v.start();}
           ,this.time);
  },
  methods:{
     gen(){
           clearInterval(this.se);
           console.log(this.arc);
            this.boo=false;
            this.$emit('teju',this.arc);
          
          
          
           

     },
     start(){
       this.boo=true
        this.arc=0;
          this.se=setInterval(()=>{this.arc=this.arc+10},10)
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
div{
  border:white;
  background-color:green;
  border-radius:8;
  height:500px;
  width:500px;
}
</style>
