<template>
  <div id="app" class="container">
   <!--TODO >>now<< Header component contai--->
   <Header :links="links"/>
   <!-- main--->
   <main>
     <!--  Jumbotron component-->
     <!-- section consultants component ( img + card component )-->
     <!-- section about us component  -->
     <!-- section project component (figure card component)-->
     <!-- section testimonial component ( testimonial card component) -->
     <!-- section blog component  (figure card component + (date + card component)-->
     <!--section lets talk component -->
   </main>
   <!-- Footer (contains links Footer + TermsFooter)--->
  </div>
</template>

<script>
import Header from './components/Header.vue';

export default {
  name: 'App',
  components: {
    Header,
  },
  data(){
    return{
      links:[
        {
          title:'home',
          link:'#',
          current:true,
        },
        {
          title:'about',
          link:'#',
          current:false,

        },
        {
          title:'product',
          link:'#',
          current:false,
          
        },
        {
          title:'services',
          link:'#',
          current:false,

        },
        {
          title:'blog',
          link:'#',
          current:false,

        },
        {
          title:'contact',
          link:'#',
          current:false,

        },
      ],
    }
  },
}
</script>

<style lang="scss">
@import '/assets/scss/style.scss';


</style>
