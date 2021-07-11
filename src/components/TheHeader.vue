<template>
  <div class="header">
    <a href="#" class="header-logo">Peace Hills</a>
    <ul>
      <li><a href="#" class="active">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Destination</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
$md-breakpoint: 1024px;
$sm-breakpoint: 768px;

.header {
  align-items: center;
  display: flex;
  left: 0;
  justify-content: space-between;
  padding: 30px 100px;
  position: absolute;
  top: 0;
  width: 100%;
  @media (max-width: $sm-breakpoint) {
    justify-content: center;
  }

  .header-logo {
    color: #094b65;
    font-size: 2em;
    font-weight: 700;
    text-decoration: none;
    z-index: 3;
  }

  ul {
    align-items: center;
    display: flex;
    justify-content: center;
    padding-inline-start: 20px;
    z-index: 3;
    @media (max-width: $sm-breakpoint) {
      display: none;
    }

    li {
      list-style: none;
      margin-left: 20px;

      a {
        color: #094b65;
        padding: 6px 15px;
        text-decoration: none;
        &:hover, &.active {
          background: #094b65;
          border-radius: 4px;
          color: white;
        }
      }
    }
  }
}
</style>
