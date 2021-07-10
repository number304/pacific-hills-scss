<template>
  <div class="container">
    <h1>The best places available</h1>
    <div class="apartment-list">
      <ApartmentCard
        v-for="(apartment, index) in apartments"
        :key="index"
        :apartment="apartment"
      />
    </div>
  </div>
</template>

<script>
import ApartmentCard from './ApartmentCard.vue'

export default {
  components: {
    ApartmentCard,
  },
  data() {
    return {
      apartments: [
        {
          name: 'Luxury Apartment',
          description: 'Only for relevant personalities, contact me.',
          author: 'Sir Tyler Baudelaire',
          photoURL: 'https://images.unsplash.com/photo-1560448204-e02f11c3d0e2?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=450&ixid=MnwxfDB8MXxyYW5kb218MHx8YXBhcnRtZW50fHx8fHx8MTYyNTg3Nzg4OQ&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=800'
        },
        {
          name: 'Pretty View Street',
          description: 'Most beautyful department in the city, for real!',
          author: 'Jhon Doe',
          photoURL: 'https://images.unsplash.com/photo-1558778909-1d4ea850da7d?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=450&ixid=MnwxfDB8MXxyYW5kb218MHx8YXBhcnRtZW50fHx8fHx8MTYyNTg3NzcyNA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=800'
        },
        {
          name: 'Elegant Apartment',
          description: 'Sober and with class, only for single people.',
          author: 'Classic Jhon Co.',
          photoURL: 'https://images.unsplash.com/photo-1460317442991-0ec209397118?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=450&ixid=MnwxfDB8MXxyYW5kb218MHx8YXBhcnRtZW50fHx8fHx8MTYyNTg3Nzc2OQ&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=800'
        },
        {
          name: 'Best City Location',
          description: 'Schedule a visit, come here and see it yourself!',
          author: 'Mary Doe',
          photoURL: 'https://images.unsplash.com/photo-1500864685331-50f6398b3c51?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=450&ixid=MnwxfDB8MXxyYW5kb218MHx8YXBhcnRtZW50fHx8fHx8MTYyNTg3Nzg2Ng&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=800'
        },
        {
          name: 'Modest Home on rent',
          description: 'I mean, is not ugly, but classical and sober',
          author: 'Gregory Terrence',
          photoURL: 'https://images.unsplash.com/photo-1493809842364-78817add7ffb?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=450&ixid=MnwxfDB8MXxyYW5kb218MHx8YXBhcnRtZW50fHx8fHx8MTYyNTg3Nzg3Ng&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=800'
        },
      ],
    }
  }
}
</script>

<style lang="scss" scoped>
.apartment-list {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  max-width: 900px;
  margin: 0 auto;
}
</style>
