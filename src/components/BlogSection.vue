<template>
  <section id="blog" class="">
    <div id="title" class="row container-sm">
      <div class="col-12">
        <div class="line-item">
          <div class="line" />
          <h5>Blog</h5>
        </div>
        <div class="line-item between">
          <h3>the recent news you must read it</h3>
          <Button title="Veiw all" type="btn-yellow" />
        </div>
      </div>
    </div>
    <div id="gallery" class="row container">
      <!-- BlogCard -->
      <CardBlog v-for="card in cards" :key="card.url" :card="card" />
    </div>
  </section>
</template>

<script>
import Button from "./Button.vue";
import CardBlog from "./CardBlog.vue";
export default {
  name: "BlogSection",
  props: ["cards"],
  components: {
    Button,
    CardBlog,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/vars";
#blog {
  margin-top: 100px;
  height: 80vh;
  #title {
    height: 20%;
    .col-12 {
      flex-basis: 100%;
      .line-item {
        display: flex;
        align-items: center;

        h5 {
          font-weight: normal;
          font-size: 0.9em;
          letter-spacing: 0.2em;
          color: $t-gray-1;
        }

        .line {
          background-color: $bg-yellow;
          width: 2%;
          height: 2px;
          margin-right: 10px;
        }
      }

      .line-item.between {
        justify-content: space-between;
      }
    }
  }
  #gallery {
    height: 60%;
    justify-content: center;
    margin-top: 30px;
  }
  .row {
    display: flex;
  }
}
</style>