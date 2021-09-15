<template>
  <section id="footer-terms">
      <div class="row">
          <div class="terms-items">
            <small> Terms of use</small>
            <small> Privacy Enviromental Policy</small>
          </div>
          <div class="copyright-items row">
            <small> Copyright  &copy;  2020, Phlax Consulting. All Rights Reserved.</small>

          </div>
      </div>
  </section>
</template>

<script>
export default {
 name:'FooterTerms',
}
</script>

<style lang="scss">
#footer-terms{
    height: 40%;
    .row{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
   
    .copyright-items small{
        align-self: flex-end;
    }
}
</style>