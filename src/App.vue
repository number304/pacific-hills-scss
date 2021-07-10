<template>
  <div id="app">
    <TheLanding :title="title" :subtitle="subtitle" />
    <ApartmentList />
  </div>
</template>

<script>
import TheLanding from './components/TheLanding.vue'
import ApartmentList from './components/ApartmentList.vue'

export default {
  name: 'App',
  components: {
    TheLanding,
    ApartmentList,
  },
  data() {
    return {
      title: 'Wanna live in the coolest city ever?',
      subtitle: 'Me too, but Peace Hills is alright. Check what appartments are available and come with us!'
    }
  }
}
</script>

<style lang="scss">
body {
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, 'Roboto', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgba($color: #000000, $alpha: 0.87);
}

.container {
  margin: 0 auto;
  padding: 30px 20px;

  &.green {
    background-color: #A9FFCB;
  }
}
</style>
