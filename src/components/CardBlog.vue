<template>
  <div class="card">
        <img src="../assets/images/startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg" alt=""/>
        <div class="box">
            <small>hjhj</small>
            <h6>hjkhjhk</h6>
            <p>hjkk</p>
        </div>
      </div>
</template>

<script>
export default {
 name:'CardBlog',
 props:['card'],
}
</script>

<style lang="scss">
.card {
    position: relative;
    text-align: justify;
    flex-basis: calc(100% / 4);
    height: 50%;
    background-color: #fff;
    margin: 0 10px;

    img {
      width: 100%;
      height: 100%;
    }
    .box {
      height: 50%;
      width: 80%;
      position: absolute;
      bottom: -15%;
      background-color: palevioletred;
      right: 0;
      padding: 30px;
    }
  }

</style>