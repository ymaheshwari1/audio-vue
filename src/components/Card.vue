<template>
  <div id="card">
    <div id="image"></div>
    <div id="content">
      <div id="title">{{ title }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: [
    'title'
  ]
}
</script>

<style scoped>
#image {
  background-image: url("../assets/logo.png");
  height: 100%;
  width: 100%;
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
}
#card {
  height: 200px;
  border-radius: 5%;
  border: 1px solid red;
  padding: 10px;
  margin: 20px 0px;
}
#content {
  margin-bottom: 20px;
  position: absolute;
  bottom: 0;
  text-align: center;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 24px;
}
</style>
