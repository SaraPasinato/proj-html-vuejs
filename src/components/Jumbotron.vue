<template>
  <section id="jumbotron">
   <div class="row">
       <div class="col-6">
           <div class="items">
               
           </div>
       </div>
       <div class="col jumbo-bg"></div>
   </div>
  </section>
</template>

<script>
export default {
 name:"Jumbotron",
}
</script>

<style lang="scss">
@import "../assets/scss/vars";
#jumbotron{
    height: 90vh;
    position: relative;
    
    .row{
        height: 100%;
        display: flex;
       
        .col{ 
            flex-basis: 100%; 
        }
       
        .col-6{ 
            flex-basis: calc(100%/2); 
               position: relative;

            .items{
                position: absolute;
                width:100%;
                height: 50%;
                background-color: palegoldenrod;
                transform: translate(-50%,-50%);
                top:50%;
                left:70%;
            }

        }
       
        .jumbo-bg{
            background-image:url('../assets/images/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg');
            background-position-x: left;
            background-size: 100%;
            background-repeat: no-repeat;
            
        }
       
    }
}
</style>