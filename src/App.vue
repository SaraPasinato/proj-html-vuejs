<template>
  <div id="app">
   <!--Header component contai >> TODO: active on click --->
   <Header :links="links"/>
   <!-- main--->
   <main>
     <!-- Jumbotron component-->

     <!-- section consultants component ( img + card component )-->
     <!-- section about us component  -->
     <!-- section project component (figure card component)-->
     <!-- section testimonial component ( testimonial card component) -->
     <!-- section blog component  (figure card component + (date + card component)-->
     <!--section lets-talk component -->
    <GetStartedSection />
   </main>
   <!-- Footer (contains links Footer + TermsFooter)--->
   <footer class="container">
    <FooterLink :links="links"/>
    <hr>
    <FooterTerms/>
   </footer>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import FooterLink from './components/FooterLink.vue';
import FooterTerms from './components/FooterTerms.vue';
import GetStartedSection from './components/GetStartedSection.vue';

export default {
  name: 'App',
  components: {
    Header,
    GetStartedSection,
    FooterLink,
    FooterTerms,
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
   height: 20vh;
   width: 100%;
}
</style>
