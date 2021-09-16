<template>
  <div id="app">
   <!--Header component contai >> TODO: active on click --->
   <Header :links="links"/>
   <!-- main--->
   <main>
     <!-- Jumbotron component-->
    <Jumbotron/>
     <!-- section consultants component (cardGoal component )-->
    <GoalsSection :cards="goalCards"/>
     <!-- section about us component  -->
    <AboutUsSection  :text="textPlaceholder"/>
    <!--  section Help component-->
    <HelpSection :text="textPlaceholderSmall"/>
     <!-- section project component ( cardFigure component)-->
    
     <!-- section testimonial component ( testimonial card component) -->
     <TestimonialSection />
     <!-- section blog component  (figure BlogCard component )-->
    <BlogSection  :cards="blogCards"/>
     <!--section lets-talk component -->
    <GetStartedSection/>
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
import BlogSection from './components/BlogSection.vue';
import TestimonialSection from './components/TestimonialSection.vue';

export default {
  name: 'App',
  components: {
    Header,
    GoalsSection,
    AboutUsSection,
    HelpSection,
    GetStartedSection,
    BlogSection,
    FooterLink,
    FooterTerms,
    Jumbotron,
    TestimonialSection,
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
      goalCards:[
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
      blogCards:[
        { 
          url:'startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg',
          date:'july 4, 2019',
          author:'paul',
          title:'Canadian Consulting From acquired by UK Giant',
          desc:'When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a...',
        },
       
        { 
          url:'business-people-working-together-on-project-and-5FHSKBL-1390.jpg',
          date:'july 4, 2019',
          author:'paul',
          title:'Canadian Consulting From acquired by UK Giant',
          desc:'When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a...',
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
