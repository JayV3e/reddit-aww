<template>
  <div>
    <h3>{{title}}</h3>
    <img :src="this.url" />
  </div>
</template>

<script>
export default {
  name: "OnePost",
  data() {
    return {
      image: null
    };
  },
  props: {
    title: {
      type: String,
      required: true
    },
    url: {
      type: String, //url
      required: true
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img {
  border-radius: 8px;
  width: 500px;
  height: 500px;
}
</style>
