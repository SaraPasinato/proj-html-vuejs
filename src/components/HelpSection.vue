<template>
  <section id="help">
   <div class="row">
       <div class="col-12">
           <div class="row-center">
               <div class="col-6 row-around">
                   <div class="box-item">
                       <h4>we help to deliver the business case</h4>
                   </div>
                   <div class="box-item">
                       <p>{{text}}</p>
                   </div>
               </div>
           </div>
        <Button  class="btnEnd" title="get started" type="btn-red"/>
       </div>
   </div>
  </section>
</template>

<script>
import Button from "./Button.vue";
export default {
  name:'HelpSection',
  props:['text'],
  components:{
      Button,
  }
}
</script>

<style lang='scss'>
@import "../assets/scss/vars";

#help{
    height: 40vh;
    background-color: transparent;

    .row{
       width:80%;
       height: 80%;
       display: flex;
       background-color:$bg-yellow;

       .col-12{
           flex-basis: 100%;
           position: relative;

        .row-center{
        width:100%;
        height: 85%;
        display: flex;
        justify-content: center;
        align-items: center;
        }

        .btnEnd{
           position: absolute;
           bottom: -20px;
           right: -10px;
           
        }
        .box-item{
            width:35%;
            text-align: start;
        }
        .col-6{
           flex-basis: 50%;
           position: relative;
        }
        .row-around{
        width:100%;
        height: 80%;
        display: flex;
        justify-content: space-around;
        align-items: center;
       
        }
    }
  }
  p{
    color: $t-dark-blue;
    font-weight: normal;
    font-size: .8em;
     padding: 0 2%;
  }
}
</style>