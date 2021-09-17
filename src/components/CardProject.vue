<template>
  <div class="card-img">
      <img :src="getImage" :alt="card.title" />
      <div class="layover">
      </div>
      <div class="items">
        <div class="row">
          <div class="col">
            <h5>{{card.title}}</h5>
            <p>{{card.category}}</p>
          </div>
          <ButtonIcon type="btn-light-blue" icon="fas fa-plus" />
        </div>
        </div>
  </div>
</template>

<script>
import ButtonIcon from '../components/ButtonIcon.vue';
export default {
  name: "CardProject",
  props: ["card"],
  components:{
    ButtonIcon,
  },
  computed: {
    getImage() {
      return require("../assets/images/" + this.card.url);
    },
  },
};
</script>

<style lang="scss">
@import '../assets/scss/vars';
.card-img {
  flex-basis: calc(100% / 4);
  background-color: #fff;
  height: 100%;
  margin: 0 2%;

  position: relative;

 
    img {
      width: 100%;
      height: 100%;
      cursor: pointer;
    }

    .layover{
      position: absolute;
      top: 0;
      left: 0;
      width:100%;
      height: 100%;
      background-color:$bg-red-dark;
      filter: saturate(1);
      opacity: 0.8;
      display: none;
    }

    .items{
        position: absolute;
        bottom:0;
        left: 0;
        z-index: 1;
        display: none;
        
        width:100%;
        height:30%;
        padding: 30px 20px;

        h5{
          text-transform: capitalize;
          font-weight: bolder;
          color: $t-light;
        }

        p{
          font-weight: lighter;
            color: $t-light-gray;
        }

        .row{
          justify-content: space-between;
        }
      }
}
.card-img:hover .items,
.card-img:hover .layover{
    display: block;
}

</style>