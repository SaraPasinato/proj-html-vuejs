<template>
  <section id="project" class="container">
       <div id="title" class="row">
      <div class="col-12">
        <div class="line-item">
          <div class="line" />
          <h5>Project</h5>
        </div>
        <div class="line-item between">
          <h3> Our expert trusted consultants help clients</h3>
          <div class="btn-items">
              <ButtonIcon  type="btn-light-blue" icon="fas fa-arrow-left" />
              <ButtonIcon  type="btn-light-blue" icon="fas fa-arrow-right" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import ButtonIcon from '../components/ButtonIcon.vue';
export default {
 name:'ProjectSection',
 components:{
     ButtonIcon,
 }
}
</script>

<style lang="scss">
@import "../assets/scss/vars";

#project{
    height: 50vh;
    margin-bottom: 40px;
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
          background-color: $t-green;
          width: 2%;
          height: 2px;
          margin-right: 10px;
        }
      }
      .line-item.between {
        justify-content: space-between;
      }
    }

    .btn-items{
        display: flex;
        justify-content: center;
    }
     }
}
</style>