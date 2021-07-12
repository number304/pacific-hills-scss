<template>
  <article class="apartment-card">
    <img :src="apartment.photoURL" alt="Apartment photo">
    <div class="apartment-card_info">
      <h2>{{ apartment.name }}</h2>
      <p>{{ apartment.description }}</p>
      <p>{{ apartment.author }}</p>
      <button class="apartment-card_cta" @click="wrongDimension">
        Contact
      </button>
    </div>
  </article>
</template>

<script>
export default {
  props: {
    apartment: {
      type: Object,
      required: true,
    }
  },
  methods: {
    wrongDimension() {
      alert('Whoops! You seem to be in a different reality. Sad.')
    }
  }
}
</script>

<style lang="scss" scoped>
.apartment-card {
  border-radius: 4px;
  box-shadow: 0 3px 1px -2px rgba(0,0,0,.2),0 2px 2px 0 rgba(0,0,0,.14),0 1px 5px 0 rgba(0,0,0,.12);
  margin: 0 10px 20px 10px;
  padding-bottom: 10px;
  width: 280px;
  min-width: 280px;
  transition: .3s cubic-bezier(.25,.8,.5,1);
    &:hover {
      box-shadow: 0 5px 5px -3px rgba(0,0,0,.2),0 8px 10px 1px rgba(0,0,0,.14),0 3px 14px 2px rgba(0,0,0,.12);
    }

  img {
    border-radius: 4px 4px 0 0;
    width: 100%;
  }


  .apartment-card_info {
    padding: 10px;

    h2, p {
      margin: 16px 0;
    }


    .apartment-card_cta {
      align-items: center;
      border-radius: 4px;
      background: #000;
      color: white;
      border: none;
      box-shadow: 0 3px 1px -2px rgb(0 0 0 / 20%), 0 2px 2px 0 rgb(0 0 0 / 14%), 0 1px 5px 0 rgb(0 0 0 / 12%);
      cursor: pointer;
      display: inline-flex;
      flex: 0 0 auto;
      font-family: 'Avenir', Helvetica, 'Roboto', sans-serif;
      font-weight: 700;
      justify-content: center;
      letter-spacing: 0.1em;
      padding: 12px 20px;
      position: relative;
      text-transform: uppercase;
      user-select: none;

      &:hover {
        background: #ff0;
        color: rgba($color: #000000, $alpha: 0.87);
      }
    }
  }
}
</style>
