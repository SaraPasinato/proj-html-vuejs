<template>
  <header>
    <div class="row container">
      <img src="../assets/images/logotype.png" alt="logo phlox" />
      <ul class="row">
        <li v-for="(link, index) in links" :key="link.title + index" @click="setCurrentIndex(index)" @click.left="$emit('choose',currentIndex)"  >
          <a :href="link.link" :class="{ active: link.current }">{{
            link.title
          }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: ["links"],
  data(){
    return{
      currentIndex:null,
    }
  },
  methods:{
    setCurrentIndex(index){
      this.currentIndex=index;
    },
  }
};
</script>

<style lang="scss">
@import "../assets/scss/vars";

header {
  height: 10vh;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1;
  background-color: transparent;

  .row {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  img {
    width: 7%;
    cursor: pointer;
  }

  li a .active {
    color: $t-light;
  }
}
</style>