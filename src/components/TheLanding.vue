<template>
  <div class="container green" id="landing-banner">
    <div id="landing-content_container">
      <div id="landing-text">
        <h1>{{ title }}</h1>
        <p>{{ subtitle }}</p>
      </div>
      <img id="city-photo" src="../assets/city-photo.jpg" alt="City photo">
    </div>
  </div>
</template>

<script>
// import cityPhoto from '../assets/city-photo.jpg'

export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      // Cause we don't have much budget to take another
      cityPhotoURL: 'https://images.unsplash.com/photo-1593007221048-141f18cf6ef6?crop=entropy&cs=tinysrgb&fm=jpg&h=900&ixid=MnwxfDB8MXxyYW5kb218MHx8dG93bnx8fHx8fDE2MjU4ODgwMzE&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=1600'
    }
  }
}
</script>

<style lang="scss" scoped>
$md-breakpoint: 1024px;
$sm-breakpoint: 768px;

#landing-banner {
  padding: 0;

  #landing-content_container {
    display: flex;
    justify-content: center;
    margin: 0 auto;
    max-width: 1200px;
    @media (max-width: $sm-breakpoint) {
      flex-direction: column;
    }

    #landing-text {
      align-items: center;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 40px;
      @media (max-width: $sm-breakpoint) {
        padding: 20px;
      }
    }

    #city-photo {
      background-size: cover;
      width: 50%;
      @media (max-width: $sm-breakpoint) {
        border: double;
        border-width: 8px;
        border-radius: 4px;
        height: auto;
        margin: 0 auto 30px auto;
        max-width: 300px;
        width: auto;
      }
    }

  }

}
</style>
