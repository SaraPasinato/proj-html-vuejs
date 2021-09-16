<template>
  <div class="card">
    <div class="items">
      <blockquote>{{ card.desc }}</blockquote>
      <cite>{{ card.author }}</cite>
      <small>{{ card.team }}</small>
      
    </div>
  </div>
</template>

<script>
export default {
  name: "CardText",
  props: ["card"],
};
</script>

<style lang="scss">
@import "../assets/scss/vars";

.card {
  flex-basis: calc(100% / 4);
  height: 70%;
  margin: 0 20px;
  .items {
    padding: 10% 15%;

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
}
</style>