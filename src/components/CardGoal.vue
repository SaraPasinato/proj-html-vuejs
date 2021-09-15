<template>
  <div class="card-goal">
    <div class="row-card">
        <img src="../assets/images/cropped-cropped-icon-270x270.png" :alt="item.title">
      <div class="col-6">
        <div class="items">
          <h5>{{item.title}}</h5>
          <p>{{item.desc}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardGoal",
  props:['item'],
};
</script>

<style lang="scss" >
@import "../assets/scss/vars";

.card-goal {
  text-align: justify;
  flex-basis: calc(100% / 2);
  height: 50%;
  

  .row-card {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    .col-6{
      flex-basis: calc(100% / 2);   
    }
    img{
      width: 10%;
      margin:0 50px 0 0;
    }
    p{
      color:$t-black;
      margin-top: 20px;
      font-size: small;
      line-height: 20px;
    }
  }
}
</style>