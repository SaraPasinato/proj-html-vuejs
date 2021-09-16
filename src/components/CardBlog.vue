<template>
  <div class="card">
        <img :src="getImage"/>
        <div class="box">
            <small>{{card.date}} by <span>{{card.author}}</span></small>
            <h6>{{card.title}}</h6>
            <p>{{card.desc}}</p>
        </div>
      </div>
</template>

<script>
export default {
 name:'CardBlog',
 props:['card'],
 computed:{
    getImage(){
      return require("../assets/images/" + this.card.url);
    }
  },
}
</script>

<style lang="scss">
@import "../assets/scss/vars";

.card {
    position: relative;
    text-align: justify;
    flex-basis: calc(100% / 4);
    height: 70%;
    background-color: #fff;
    margin: 0 10px;

    img {
      width: 100%;
      height: 100%;
    }
    .box {
      height: 60%;
      width: 80%;
      position: absolute;
      bottom: -20%;
      background-color: $bg-light;
      right: 0;
      padding: 30px 50px;

      p{
      color:$t-gray-6;
      font-size: x-small;
      line-height: 15px;
      text-align: start;
      }
      small{
          color:$t-red;
      }
      span{
          margin-left:10px;
      }
    }
  }

</style>