<template>
  <section id="project" >
    <div id="title" class="row container-sm">
      <div class="col-12">
        <div class="line-item">
          <div class="line" />
          <h5>Project</h5>
        </div>
        <div class="line-item between">
          <h3>Our expert trusted consultants help clients</h3>
          <div class="btn-items">
            <ButtonIcon type="btn-light-blue" icon="fas fa-arrow-left" />
            <ButtonIcon type="btn-light-blue" icon="fas fa-arrow-right" />
          </div>
        </div>
      </div>
    </div>
    <div id="gallery" class="row container-sm">
      <CardProject  :key="index" v-for="(card,index) in cards" :card="card"/>
    </div>
  </section>
</template>

<script>
import ButtonIcon from "../components/ButtonIcon.vue";
import CardProject from "../components/CardProject.vue";
export default {
  name: "ProjectSection",
  props:['cards'],
  components: {
    ButtonIcon,
    CardProject,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/vars";

#project {
  height: 50vh;
  margin-bottom: 10%;
  #title {
    height: 20%;
    .col-12 {
      flex-basis: 100%;
      .line-item {
        display: flex;
        align-items: center;

        h5 {
          font-weight: normal;
          font-size: 0.9em;
          letter-spacing: 0.2em;
          color: $t-gray-1;
        }

        .line {
          background-color: $bg-yellow;
          width: 2%;
          height: 2px;
          margin-right: 10px;
        }
      }
      .line-item.between {
        justify-content: space-between;
      }
    }

    .btn-items {
      display: flex;
      justify-content: center;
    }
  }
  #gallery{
      margin-top: 5%;
      height: 70%;
      align-items: center;
      justify-content: center;
  }

  .row{
    display: flex;
  }
}
</style>