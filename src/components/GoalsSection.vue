<template>
  <section id="goals">
  <div class="row-start container-sm">
      <div class="col"> 
          <h4>Our Consultants can help you</h4>
      </div>
  </div>
  <div class="row container-sm">
      <div class="col"> 
          <!-- TODO cards components -->
          <h4>Our Consultants can help you</h4>
      </div>
  </div>
  </section>
</template>

<script>
export default {
  name:'GoalsSection',
}
</script>

<style lang="scss">
@import '../assets/scss/vars';
#goals{
    height: 80vh;
    width:100%;
    padding: 100px;
    background-color: $bg-light;

    .row-start {
    height: 20%;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-wrap: wrap;
    }
    .row {
    height: 80%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    background-color: palegoldenrod;
    }

    h4{
        color: $t-black;
        font-size: 1.7em;
        text-transform: uppercase;
        
    }
}
</style>