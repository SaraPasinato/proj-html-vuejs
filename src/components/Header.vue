<template>
  <header  class="container">
    <div class="row">
    
      <img src="../assets/images/logotype.png" alt="logo phlox" />

      <ul class="row">
        <li
          v-for="(link, index) in links"
          :key="link.title + index"
          
        >
          <a :href="link.link" :class="{ active: link.current }">{{ link.title }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: ["links"],
  //TODO: set active on click 
};
</script>

<style lang="scss">
@import "../assets/scss/vars";

header {
  height: 10vh;
  background-color: transparent;
  position: absolute;
  top: 0;
  left: 100px;
  width: 100%;
  z-index: 1;
  
  .row {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  img {
    width: 7%;
  }

  li a .active{
    color: $t-light;
  }
}
</style>