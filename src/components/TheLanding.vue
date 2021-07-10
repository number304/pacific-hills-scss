<template>
  <div class="container" id="landing-banner">
    <div id="landing-content_container">
      <div id="landing-text">
        <h1>Wanna live in the <span>coolest</span> city ever?</h1>
        <p>Me too, but Peace Hills is alright.</p>
      </div>
      <!-- <a href="#" class="">Explore</a> -->
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Mogra&display=swap');

$md-breakpoint: 1024px;
$sm-breakpoint: 768px;

#landing-banner {
  padding: 0;

  #landing-content_container {
    align-items: center;
    display: flex;
    justify-content: center;
    position: relative;
    min-height: 100vh;
    width: 100%;
    @media (max-width: $sm-breakpoint) {
      flex-direction: column;
    }

    #landing-text {
      position: absolute;
      color: #094b65;
      font-size: 10vw;
      text-align: center;
      padding: 40px;
      h1 {
        font-size: 0.4em;
        span {
          font-family: 'Mogra', 'Avenir', Helvetica, 'Roboto', sans-serif;
        }
      }
      p {
        font-size: 0.2em;
        letter-spacing: 1px;
        font-weight: 400;
      }
      @media (max-width: $sm-breakpoint) {
        padding: 20px;
        h1 {
          font-size: 0.8em;
        }
        p {
          font-size: 0.4em;
        }
      }
    }

  }

}
</style>
