<template>
  <div>
    <Header />
    <Slider />
  </div>
</template>

<script>
import Header from './Header'
import Slider from './Slider'

export default {
  name: 'Home',
  components: {
    Header,
    Slider
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
