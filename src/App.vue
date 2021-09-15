<template>
  <div id="app" class="container">
   <!--Header component contai >> TODO: active on click --->
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
   <!--TODO >>now<< Footer (contains links Footer + TermsFooter)--->
   <footer>
    <FooterLink :links="links"/>
   </footer>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import FooterLink from './components/FooterLink.vue';

export default {
  name: 'App',
  components: {
    Header,
    FooterLink,
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

footer{
   height: 50vh;
   width: 100%;
}
</style>
