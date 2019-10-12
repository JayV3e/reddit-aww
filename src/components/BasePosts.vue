<template>
  <div>
    <!-- <OnePost
      v-for="post in postsData"
      :key="post.id"
      :title="post['data']['title']"
      :url="post['data']['url']"
    />-->
    <OnePost :title="postsData[0]['data']['title']" :url="postsData[0]['data']['url']" />
  </div>
</template>

<script>
import axios from "axios";
import OnePost from "./OnePost";

export default {
  name: "BasePosts",
  components: {
    OnePost
  },
  data() {
    return {
      postsData: null
    };
  },
  mounted() {
    axios
      .get("https://www.reddit.com/r/aww.json")
      .then(
        response => (this.postsData = response["data"]["data"]["children"])
      );
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
