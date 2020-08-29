<template>
  <div id="slider">
    <div id="heading">Category 1</div>
    <vue-glide
      :perView=5
      :bound=true
      :breakpoints="{
        400:{
          perView:2
        },
        800:{
          perView:3
        }
      }"
    >
      <vue-glide-slide v-for="i in 10" :key="i">
        <Card @click.native="cardClicked(titles[i-1])"
          :title="titles[i-1]"
        />
      </vue-glide-slide>
      <template slot="control">
        <button id="prev" data-glide-dir="<">
          <img src="../assets/left.svg" alt="prev">
        </button>
        <button id="next" data-glide-dir=">">
          <img src="../assets/right.svg" alt="next">
        </button>
      </template>
    </vue-glide>

    <div id="heading">Category 2</div>
    <vue-glide
      :perView=5
      :bound=true
      :breakpoints="{
        400:{
          perView:2
        },
        800:{
          perView:3
        }
      }"
    >
      <vue-glide-slide v-for="i in 10" :key="i">
        <Card @click.native="cardClicked(titles[i-1])"
          :title="titles[i-1]"
        />
      </vue-glide-slide>
      <template slot="control">
        <button id="prev" data-glide-dir="<">
          <img src="../assets/left.svg" alt="prev">
        </button>
        <button id="next" data-glide-dir=">">
          <img src="../assets/right.svg" alt="next">
        </button>
      </template>
    </vue-glide>

    <div id="heading">Category 3</div>
    <vue-glide
      :perView=5
      :bound=true
      :breakpoints="{
        400:{
          perView:2
        },
        800:{
          perView:3
        }
      }"
    >
      <vue-glide-slide v-for="i in 10" :key="i">
        <Card @click.native="cardClicked(titles[i-1])"
          :title="titles[i-1]"
        />
      </vue-glide-slide>
      <template slot="control">
        <button id="prev" data-glide-dir="<">
          <img src="../assets/left.svg" alt="prev">
        </button>
        <button id="next" data-glide-dir=">">
          <img src="../assets/right.svg" alt="next">
        </button>
      </template>
    </vue-glide>

    <div id="heading">Category 4</div>
    <vue-glide
      :perView=5
      :bound=true
      :breakpoints="{
        400:{
          perView:2
        },
        800:{
          perView:3
        }
      }"
    >
      <vue-glide-slide v-for="i in 10" :key="i">
        <Card @click.native="cardClicked(titles[i-1])"
          :title="titles[i-1]"
        />
      </vue-glide-slide>
      <template slot="control">
        <button id="prev" data-glide-dir="<">
          <img src="../assets/left.svg" alt="prev">
        </button>
        <button id="next" data-glide-dir=">">
          <img src="../assets/right.svg" alt="next">
        </button>
      </template>
    </vue-glide>
    <Modal ref="modal"/>
  </div>
</template>

<script>
import Card from './Card'
import Modal from './Modal'

export default {
  name: 'Slider',
  data () {
    return {
      titles: ['card1', 'card2', 'card3', 'card4', 'card5', 'card6', 'card7', 'card8', 'card9', 'card10']
    }
  },
  components: {
    Card,
    Modal
  },
  methods: {
    cardClicked: function (title) {
      this.$refs.modal.show(title)
    }
  }
}
</script>

<style scoped>
#slider {
  padding: 10px;
}
#next {
float: right;
}
#prev, #next {
  border: none;
  background: transparent;
}
#heading {
  font-size: 48px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
</style>
