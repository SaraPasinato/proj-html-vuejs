<template>
  <div id="app">
    <!--Header component contai >> TODO: fix header --->
    <Header :links="links" @choose="setActive" />
    <!-- main--->
    <main>
      <!-- Jumbotron component-->
      <Jumbotron />
      <!-- section consultants component (cardGoal component )-->
      <GoalsSection :cards="goalCards" />
      <!-- section about us component  -->
      <AboutUsSection :text="textPlaceholder" />
      <!--  section Help component-->
      <HelpSection :text="textPlaceholderSmall" />
      <!-- section project component ( cardFigure component)-->
      <ProjectSection :cards="projectCards" />
      <!-- section testimonial component ( testimonial card component) -->
      <TestimonialSection :cards="userCards" />
      <!-- section blog component  (figure BlogCard component )-->
      <BlogSection :cards="blogCards" />
      <!--section lets-talk component -->
      <GetStartedSection />
    </main>
    <!-- Footer (contains links Footer + TermsFooter)--->
    <footer class="container-sm">
      <FooterLink :links="links" />
      <hr />
      <FooterTerms />
    </footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import FooterLink from "./components/FooterLink.vue";
import FooterTerms from "./components/FooterTerms.vue";
import GetStartedSection from "./components/GetStartedSection.vue";
import GoalsSection from "./components/GoalsSection.vue";
import Jumbotron from "./components/Jumbotron.vue";
import AboutUsSection from "./components/AboutUsSection.vue";
import HelpSection from "./components/HelpSection.vue";
import BlogSection from "./components/BlogSection.vue";
import TestimonialSection from "./components/TestimonialSection.vue";
import ProjectSection from "./components/ProjectSection.vue";

export default {
  name: "App",
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
    ProjectSection,
  },
  data() {
    return {
      textPlaceholder:
        "When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed when I hear the buzz of the little world among the staks, and grow familiar inderscibable forms of  the insects and flies, then I feel  the presence of the Alimighty.",
      textPlaceholderSmall:
        "When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown ",
      links: [
        {
          title: "home",
          link: "#jumbotron",
          current: true,
        },
        {
          title: "about",
          link: "#about-us",
          current: false,
        },
        {
          title: "product",
          link: "#project",
          current: false,
        },
        {
          title: "services",
          link: "#goals",
          current: false,
        },
        {
          title: "blog",
          link: "#blog",
          current: false,
        },
        {
          title: "contact",
          link: "#get-started",
          current: false,
        },
      ],
      goalCards: [
        {
          url: "cropped-cropped-icon-270x270.png",
          title: "Statistical consuliting",
          desc: "When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a",
        },
        {
          url: "cropped-cropped-icon-270x270.png",
          title: "banking consulting",
          desc: "When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a",
        },
        {
          url: "cropped-cropped-icon-270x270.png",
          title: "Digital Consulting",
          desc: "When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a",
        },
        {
          url: "cropped-cropped-icon-270x270.png",
          title: "Enterprise consuliting",
          desc: "When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a",
        },
      ],
      blogCards: [
        {
          url: "startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg",
          date: "july 4, 2019",
          author: "paul",
          title: "Canadian Consulting From acquired by UK Giant",
          desc: "When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a...",
        },

        {
          url: "business-people-working-together-on-project-and-5FHSKBL-1390.jpg",
          date: "july 4, 2019",
          author: "paul",
          title: "Canadian Consulting From acquired by UK Giant",
          desc: "When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a...",
        },
      ],
      userCards: [
        { 
          url:'oliver-ragfelt-488196-2.jpg',
          team: "Amazon Inc.",
          author: "Vera Ducan",
          title: "Canadian Consulting From acquired by UK Giant",
          desc: "When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a thousand unknown plants are noticed when I hear the buzz of the little",
        },
        {
           url:'oliver-ragfelt-488196-unsplash.jpg',
          team: "Amazon Inc.",
          author: "Vera Ducan",
          title: "Canadian Consulting From acquired by UK Giant",
          desc: "When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a thousand unknown plants are noticed when I hear the buzz of the little",
        },
        {
          url:'12679.jpg',
          team: "Amazon Inc.",
          author: "Vera Ducan",
          title: "Canadian Consulting From acquired by UK Giant",
          desc: "When,while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable follage of my trees,and but a thousand unknown plants are noticed when I hear the buzz of the little",
        },
      ],
      projectCards: [
        {
          url: "221bf0b7-8134-43bb-936a-5acbe42db64a-790x592.jpg",
          title: "Purinky Products",
          category: "uncategorized",
        },
        {
          url: "DRY-1-790x592.jpg",
          title: "Photography Products",
          category: "photo",
        },
        {
          url: "z1el4c4p-790x592.jpg",
          title: "Vizeon Products",
          category: "web",
        },
      ],
    };
  },
  methods: {
    setActive(index) {
      //setto tutti i current a false
      this.links.forEach((el) => {
        el.current = false;
      });
      this.links[index].current = !this.links[index].current;
    },
  },
};
</script>

<style lang="scss">
@import "/assets/scss/style.scss";
#app {
  position: relative;
  width: 100%;
}

footer {
  height: 20vh;
  width: 100%;
}
</style>
