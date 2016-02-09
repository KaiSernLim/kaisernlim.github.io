<template id="site-footer">
  <footer class="site-footer">
    <div class="container">
      <div class="row">
        <div class="four columns">
          <p class="no-margin">Copyright © {{ year }} Kai-Sern Lim</p>
        </div>
        <div class="four columns">
          <p class="no-margin"><i class="fa fa-map-marker"></i> San Jose, CA</p>
        </div>
        <div class="four columns">
          <a href="http://kaisernlim.com"><i class="fa fa-home"></i> kaisernlim.com</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data () {
    return {
      year: new Date().getFullYear().toString()
    }
  }
}
</script>

<style lang="sass?indentedSyntax">
  .site-footer
    right: 0
    bottom: 0
    left: 0
    padding: 2rem 0px
    background-color: #efefef
    text-align: center
</style>
