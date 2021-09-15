<template>
  <div>
       <button class="btn" :class="type">{{title}}</button>
  </div>
</template>

<script>

export default {
  name:'Button',
  props:['title','type'],
}
</script>

<style lang="scss">
@import "../assets/scss/vars";

</style>