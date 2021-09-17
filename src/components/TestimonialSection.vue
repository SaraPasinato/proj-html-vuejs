<template>
  <section id="testimonial">
    <div id="title" class="row container-sm">
      <div class="col-12">
        <div class="line-item">
          <h5>Testimonial</h5>
          <div class="line" />
        </div>
        <div class="line-item">
          <h3>What's the customer say <br />about our work</h3>
        </div>
      </div>
    </div>
    <div id="gallery" class="row container">
      <CardText v-for="(card, index) in cards" :key="index" :card="card" />
    </div>
  </section>
</template>

<script>
import CardText from "../components/CardText.vue";
export default {
  name: "TestimonialSection",
  props: ["cards"],
  components: {
    CardText,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/vars";

#testimonial {
  height: 60vh;
  margin-bottom: 80px;

  #title {
    height: 30%;
    .line-item {
      display: flex;
      align-items: center;
      justify-content: space-between;
      text-align: right;
      h5 {
        font-weight: normal;
        font-size: 0.9em;
        letter-spacing: 0.2em;
        color: $t-gray-1;
      }

      .line {
        background-color: $bg-yellow;
        width: 7%;
        height: 2px;
        margin-right: 1px;
      }
    }
  }

  #gallery {
    height: 70%;
    margin-left: 20%;
    margin-top: 40px;
    width: 80%;
    justify-content: flex-end;
    align-items: center;
    background-color: $bg-light;
    padding-left: 10px;
  }
  .row {
    display: flex;
    flex-direction: row-reverse;
  }
}
</style>