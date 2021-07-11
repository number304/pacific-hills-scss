<template>
  <div class="container" id="landing-banner">
    <div id="landing-content_container">
      <div id="landing-text">
        <h1>Wanna live in the <span>coolest</span> city ever?</h1>
        <p>Me too, but Peace Hills is alright.</p>
      </div>
      <a href="#" class="landing-cta">Explore</a>
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
$xs-breakpoint: 420px;

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
      color: #094b65;
      font-size: 10vw;
      padding: 40px;
      position: absolute;
      text-align: center;
      transform: translateY(-20%);
      h1 {
        font-size: 0.4em;
        span {
          font-family: 'Mogra', 'Avenir', Helvetica, 'Roboto', sans-serif;
        }
      }
      p {
        font-size: 0.2em;
        font-weight: 400;
        letter-spacing: 1px;
      }
      @media (max-width: $sm-breakpoint) {
        padding: 30px;
        h1 {
          font-size: 0.8em;
        }
        p {
          font-size: 0.4em;
        }
      }
    }

    .landing-cta {
      background: #ff0;
      border-radius: 4px;
      color: #094b65;
      display: inline-block;
      font-size: 1.1em;
      font-weight: 700;
      letter-spacing: 1px;
      padding: 8px 30px;
      text-decoration: none;
      transform: translateY(80px);
      @media (max-width: $md-breakpoint) {
        transform: translateY(60px);
      }
      @media (max-width: $sm-breakpoint) {
        transform: translateY(100px);
        font-size: 1em;
      }
      @media (max-width: $xs-breakpoint) {
        transform: translateY(60px);
        font-size: 0.8em;
      }
    }

  }

}
</style>
