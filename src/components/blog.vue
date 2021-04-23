<template>
<div id="blog" class="container">
<form >
  <div class="form-group">
    <h1>Blog Post</h1>
    <label for="exampleFormControlInput1">Title</label>
    <input type="text" class="form-control" id="exampleFormControlInput1" v-model.lazy="blog.title" placeholder="title">
  </div>


<div class="form-check form-check-inline">
  <input class="form-check-input" type="checkbox" id="inlineCheckbox1" value="Advanced"  v-model="blog.audience">
  <label class="form-check-label" for="inlineCheckbox1">Advanced</label>
</div>
<div class="form-check form-check-inline">
  <input class="form-check-input" type="checkbox" id="inlineCheckbox2" value="Novice" v-model="blog.audience">
  <label class="form-check-label" for="inlineCheckbox2">Novice</label>
</div>



  
  <div class="form-group">
    <label for="exampleFormControlTextarea1">Content</label>
    <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"  v-model="blog.content" ></textarea>
  </div>
  <div>
    <button class="btn btn-primary mt-4 ">Post</button>
  </div>

  
</form>
  <div class="form-group">
    <label for="exampleFormControlTextarea1"  class="h2 ">Preview</label>
   <p>Blog Title:{{ blog.title}}</p>
   <p>Blog Content: {{blog.content}}</p>
  </div>

<div v-for="aud in blog.audience" :key="aud">
  <p>aud</p>

</div>
</div>

    </template>

<script>
export default {

  data () {
    return {
       blog:{
         title:"",
         content:"",
         audience:[]
       }
    }
  }
}

</script>

<style scoped>

</style>
