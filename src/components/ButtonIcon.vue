<template>
  <div>
       <button class="btn-icon" :class="type"><i :class="icon"></i></button>
  </div>
</template>

<script>

export default {
  name:'ButtonIcon',
  props:['type','icon'],
}
</script>

<style lang="scss">
@import "../assets/scss/vars";

</style>