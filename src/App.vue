<template>
  <div id="app">
   <!--Header component contai >> TODO: active on click --->
   <Header :links="links"/>
   <!-- main--->
   <main>
     <!-- Jumbotron component-->
    <Jumbotron/>
     <!-- section consultants component (cardGoal component )-->
    <GoalsSection :cards="goalCard"/>
     <!-- section about us component  -->
    <AboutUsSection  :text="textPlaceholder"/>
    <!--  section Help component-->
    <HelpSection :text="textPlaceholderSmall"/>
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
import Jumbotron from './components/Jumbotron.vue';
import AboutUsSection from './components/AboutUsSection.vue';
import HelpSection from './components/HelpSection.vue';

export default {
  name: 'App',
  components: {
    Header,
    GoalsSection,
    AboutUsSection,
    HelpSection,
    GetStartedSection,
    FooterLink,
    FooterTerms,
    Jumbotron,
  },
  data(){
    return{
      textPlaceholder:'When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed when I hear the buzz of the little world among the staks, and grow familiar inderscibable forms of  the insects and flies, then I feel  the presence of the Alimighty.',
      textPlaceholderSmall:'When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown ',
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
          url:'cropped-cropped-icon-270x270.png',
          title:'Statistical consuliting',
          desc:'When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a',
        },
        {
          url:'cropped-cropped-icon-270x270.png',
          title:'banking consulting',
          desc:'When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a',
        },
        {
          url:'cropped-cropped-icon-270x270.png',
          title:'Digital Consulting',
          desc:'When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a',
        },
        {
          url:'cropped-cropped-icon-270x270.png',
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
#app{
  position: relative;
}

footer{
   height: 20vh;
   width: 100%;
}
</style>
