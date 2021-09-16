<template>
  <section id="get-started">
    <div class="row">
      <div class="col">
        <h3>Let's talk about work</h3>
        <div class="items">
            <p>
              A wonderful serenity has taken possession
              Far far away, behaind the
              word mountains.
            </p>
           <Button title='get started' type="btn-dark"/>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Button from './Button.vue';
export default {
  name: "GetStartedSection",
  components:{
    Button,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/vars";
#get-started {

  height: 40vh;
  width: 100%;

  background-image: url("../assets/images/business-people-working-together-on-project-and-B3MZ4TX.jpg");
  background-position: center;
  background-size: cover;
  text-align: center;

  .row {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;

     .col{
       
       .items{
           padding: 0 15%;

       }
    }
  }

 
}
</style>