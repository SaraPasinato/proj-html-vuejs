<template>
  <section id="testimonial" class="container">
 <div id="title" class="row">
      <div class="col-12">
        <div class="line-item">
          <h5>Testimonial</h5>
          <div class="line" />
        </div>
        <div class="line-item">
          <h3>What's the customer say about our work</h3>

        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
    name:"TestimonialSection",
    props:['cards'],
}
</script>

<style lang="scss">
@import '../assets/scss/vars';

#testimonial{
    height: 50vh;
    background-color: palevioletred;
    margin-bottom: 80px;

    #title {
        height: 30%;
        .line-item {
        display: flex;
        align-items: center;
        justify-content: space-between;
        h5 {
          font-weight: normal;
          font-size: 0.9em;
          letter-spacing: 0.2em;
          color: $t-gray-1;
        }

        .line {
          background-color: $t-green;
          width: 4%;
          height: 2px;
          margin-right: 10px;
        }
      }

    }
    .row {
    display: flex;
    flex-direction: row-reverse;
    }
}
</style>