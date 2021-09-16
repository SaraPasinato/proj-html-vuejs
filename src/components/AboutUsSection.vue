<template>
  <section id="about-us">
   <div class="row">
       <div class="col img-bg"></div>
       <div class="col-6">
           <div class="items">
               <div class="line-title">
                   <div class="line"/>
                   <h5> About us</h5>
               </div>
               <h2> we make your strategy work</h2>
               <p>{{text}}</p>
           </div>
       </div>
       
   </div>
  </section>
</template>

<script>

export default {
 name:"AboutUsSection",
 props:["text"],
}
</script>

<style lang="scss">
@import "../assets/scss/vars";
#about-us{
    height: 60vh;
    position: relative;
    
    .row{
        height: 100%;
        display: flex;
       
        .col{ 
            flex-basis: 100%; 
        }
       
        .col-6{ 
            flex-basis: calc(100%/12 * 10); 
            position: relative;

            .items{
                position: absolute;
                width:50%;
                height: 50%;
                transform: translate(-50%,-50%);
                top:40%;
                left:35%;


                h5{
                    font-weight: normal;
                    font-size: .9em;
                    letter-spacing: 0.2em;
                    color:$t-gray-1;
                }
                p{
                    font-weight: normal;
                    font-size: .9em;
                    padding: 0 2%;
                }
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
       
        .img-bg{
            background-image:url('../assets/images/business-people-working-together-on-project-and-5FHSKBL.jpg');
            background-size: cover;
            background-repeat: no-repeat;
          
        }
       
    }
}
</style>