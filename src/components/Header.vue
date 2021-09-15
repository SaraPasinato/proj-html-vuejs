<template>
  <header  class="container">
    <div class="row">
      <img src="../assets/images/logotype.png" alt="logo phlox" />

      <ul class="row">
        <li
          v-for="(link, index) in links"
          :key="link.title + index"
          :class="{ active: link.current }"
        >
          <a :href="link.link">{{ link.title }}</a>
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
header {
  height: 10vh;
  border: 2px solid white;
  background-color: transparent;

  .row {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  img {
    width: 7%;
  }
}
</style>