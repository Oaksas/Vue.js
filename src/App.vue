<template>

    <div>
<app-header></app-header>
  <app-blog ></app-blog>
  <app-footer></app-footer>
    </div>
</template>

<script>
import Blog from './components/blog.vue';
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';



export default {
  components:{

  'app-blog':Blog,
  'app-header':Header,
  'app-footer':Footer

},
  data () {
    return {
      title:"Vue Intro",

    }
  },
  methods:{
    updateTitle:function(updatedTitle){
      this.title=updatedTitle;

    }
  },
 
 
 
 
}
</script>

<style>

</style>
