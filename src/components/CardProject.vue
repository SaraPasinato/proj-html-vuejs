<template>
  <div class="card-img">
    <img :src="getImage" :alt="card.title" />
  </div>
</template>

<script>
export default {
  name: "CardProject",
  props: ["card"],
  computed: {
    getImage() {
      return require("../assets/images/" + this.card.url);
    },
  },
};
</script>

<style lang="scss">
.card-img {
  flex-basis: calc(100% / 4);
  background-color: #fff;
  height: 100%;
  margin: 0 2%;
  img {
    width: 100%;
    height: 100%;
    cursor: pointer;
  }
}
</style>