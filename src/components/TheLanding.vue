<template>
  <div class="container" id="landing-banner">
    <div id="landing-content_container">
      <div id="landing-text">
        <h1>Wanna live in the <span>coolest</span> city ever?</h1>
        <p>Me too, but Peace Hills is alright.</p>
      </div>
      <img src="../assets/forest.png" alt="Forest" id="landing-forest">
      <a href="#" id="landing-cta">Explore</a>
      <img src="../assets/rocks.png" alt="Rocks" id="landing-rocks">
      <img src="../assets/lake.png" alt="Lake" id="landing-lake">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      landingText: null,
      button: null,
      rocks: null,
    }
  },
  mounted() {
    this.landingText = document.getElementById('landing-text')
    this.button = document.getElementById('landing-cta')
    this.rocks = document.getElementById('landing-rocks')

    window.addEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll () {
      let value = window.scrollY

      this.landingText.style.top = 250 + value * -1 + 'px'
      this.button.style.marginTop = value * 1.5 + 'px'
      this.rocks.style.top = value * -0.05 + 'px'

      if (value > 300) this.button.style.display = 'none'
      else this.button.style.display = 'inline-block'
    }
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll);
  }
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Mogra&display=swap');

$md-breakpoint: 1024px;
$sm-breakpoint: 768px;
$xs-breakpoint: 425px;

#landing-banner {
  padding: 0;

  #landing-content_container {
    align-items: center;
    display: flex;
    justify-content: center;
    position: relative;
    height: 100vh;
    width: 100%;
    @media (max-width: $sm-breakpoint) {
      flex-direction: column;
    }

    #landing-text {
      font-size: 10vw;
      padding: 40px;
      position: absolute;
      text-align: center;
      transform: translateY(-40%);
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

    img {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      object-fit: cover;
    }

    #landing-forest {
      top: 80px;
      @media (max-width: $md-breakpoint) {
        top: 60px;
      }
      @media (max-width: $sm-breakpoint) {
        top: 80px;
      }
      @media (max-width: $xs-breakpoint) {
        top: 40px;
      }
    }

    #landing-cta {
      background: #ff0;
      border-radius: 4px;
      color: rgba($color: #000000, $alpha: 0.87);
      display: inline-block;
      font-size: 1.1em;
      font-weight: 700;
      letter-spacing: 1px;
      padding: 12px 20px;
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
