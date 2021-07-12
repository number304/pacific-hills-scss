<template>
  <div id="footer">
    <h2>Peace Hills</h2>
    <p id="subtitle">You don't need something great, fine is ok.</p>
    <div class="divider"></div>
    <p id="attribution">
      Made with love by
       <a target="_blank" href="https://www.linkedin.com/in/jose-miguel-pedraza-mateo-n304/?locale=en_US">
        Jose Miguel
      </a>
    </p>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
#footer {
  background: #000;
  color: white;
  padding: 20px;

  #subtitle {
    padding-bottom: 10px;
  }

  .divider {
    background-color: white;
    height: 2px;
    margin: 0 auto;
    width: 200px;
  }

  #attribution {
    padding-top: 10px;
    a {
      color: white;
    }
  }
}
</style>
