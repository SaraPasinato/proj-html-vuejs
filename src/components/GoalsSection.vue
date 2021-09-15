<template>
  <section id="goals">
    <div class="container-sm">
      <h4>Our consultants can help you</h4>
      <div class="row">
       <CardGoal v-for="card in cards" :key="card.title" :item="card"/>
    
      </div>
    </div>
  </section>
</template>

<script>
import CardGoal from "./CardGoal.vue";

export default {
  name: "GoalsSection",
  props:["cards"],
  components: {
    CardGoal,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/vars";
#goals {
  height: 80vh;
  width: 100%;
  padding: 50px 0;
  background-color: $bg-light;

  .row {
    height: 60vh;
    margin-top: 4em;

    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;

  
  }
  
}
</style>