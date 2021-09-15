<template>
  <div id="app">
   <!--Header component contai >> TODO: active on click --->
   <Header :links="links"/>
   <!-- main--->
   <main>
     <!-- Jumbotron component-->
    
     <!-- >>TODO<< section consultants component ( img + card component )-->
    <GoalsSection :cards="goalCard"/>
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
import GoalsSection from './components/GoalsSection.vue';

export default {
  name: 'App',
  components: {
    Header,
    GoalsSection,
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
      goalCard:[
        { 
          title:'Statistical consuliting',
          desc:'When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a',
        },
        {
          title:'banking consulting',
          desc:'When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a',
        },
        {
          title:'Digital Consulting',
          desc:'When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a',
        },
        {
          title:'Enterprise consuliting',
          desc:'When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a',
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
