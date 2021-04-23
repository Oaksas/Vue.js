
<template>
<header>
    <nav class="navbar navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand">Navbar</a>
    <form class="d-flex">
      <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
      <button class="btn btn-outline-success" type="submit">Search</button>
    </form>
  </div>
</nav>
</header>
    </template>

<script>
import {bus} from '../main';
export default {
    props:{
        title:{
            type:String
        }
    },
  data () {
    return {
    }
  },
  methods:{
      changeTitle:function(){
  
          this.title="Vue Changed";
          bus.$emit('titleChanged','Vue Changed')
      }
  }
}
</script>

<style scoped>
header{
    background-color:black;
    
}
h1{
    color:white;
}
</style>
