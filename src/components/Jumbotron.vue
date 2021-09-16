<template>
  <section id="jumbotron">
   <div class="row">
       <div class="col-6">
           <div class="items">
               <div class="line-title">
                   <div class="line"/>
                   <h5> always te best way you need it</h5>
               </div>
               <h1> the best business consulting</h1>
               <div class="btn-control">
                   <Button type="btn-green" title="Read more"/>
                   <ButtonIcon type="btn-outline-green circle" icon="fas fa-play"/>
               </div>
           </div>
       </div>
       <div class="col jumbo-bg"></div>
   </div>
  </section>
</template>

<script>
import Button from './Button.vue';
import ButtonIcon from './ButtonIcon.vue';
export default {
 name:"Jumbotron",
 components:{
     Button,
     ButtonIcon,
 }
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
                width:80%;
                height: 50%;
                transform: translate(-50%,-50%);
                top:50%;
                left:80%;


                h5{
                    font-weight: normal;
                    font-size: .9em;
                    letter-spacing: 0.2em;
                    color:$t-gray-1;
                }
                .btn-control,
                .line-title{
                    display: flex;
                    align-items: center;
                }
               .line{
                  background-color:$t-green;
                  width:7%;
                  height: 2px;
                  margin-right: 10px;
               }

             
            }

        }
       
        .jumbo-bg{
            background-image:url('../assets/images/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg');
            background-position: top ;
            background-size: cover;
            background-repeat: no-repeat;
            
        }
       
    }
}
</style>