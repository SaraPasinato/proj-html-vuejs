<template>
  <div class="card">
    <div class="items">
      <blockquote>{{ card.desc }}</blockquote>
      <cite>{{ card.author }}</cite>
      <small>{{ card.team }}</small>  
    </div>
    <div class="laydown">
      <img :src="getImage" :alt="card.author">
    </div>
  </div>
</template>

<script>
export default {
  name: "CardText",
  props: ["card"],
  computed: {
    getImage() {
      return require("../assets/images/" + this.card.url);
    },
  },
};
</script>

<style lang="scss">
@import "../assets/scss/vars";

.card {
  position: relative;
  flex-basis: 23%;
  height: 82%;
 // margin: 0 20px;

  .items {
    position: absolute;
    top: 20%;
    left: 0;
    z-index: 2;

    width: 100%;
    height: 100%;
    padding: 0 15%;

    blockquote{
      margin-bottom:30px;
      font-style: normal;
      color: $t-gray-7;
      font-size: small;
      line-height: 15px;
      text-align: start;
      font-weight: lighter;
    }

    small{
       color: $t-gray-7;
    }
  }

  .laydown{
    display: none;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;

    img{
      width: 100%;
      height: 100%;
      opacity: 0.9;
    }
  }
}

.card:hover .laydown {
  display: block;
}

.card:hover  small,
.card:hover  blockquote{
   color: $t-gray-1;
   font-weight: normal;
   line-height: 20px;
}
.card:hover cite{
   color: $t-light;
   font-weight: bolder;
   font-size: 20px;
}
</style>