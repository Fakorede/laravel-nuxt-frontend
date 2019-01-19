<template>
    <div class="container">
        <h2>Latest Topics</h2>
        <div class="bg-light mt-5 mb-5" v-for="(topic, index) in topics" :key="index" style="padding: 20px;">
            <h2>{{topic.title}}</h2>
            <p class="text-muted">{{topic.created_at}} by {{topic.user.name}}</p>
            <div class="ml-5 content" v-for="(content, index) in topic.posts" :key=index>
                {{content.body}}
                <p class="text-muted">{{content.created_at}} by {{content.user.name}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      topics: []
    };
  },
  async asyncData({ $axios }) {
    let { data } = await $axios.$get("/topics");
    return {
      topics: data
    };
  }
};
</script>

<style>
.content {
  border-left: 10px solid #fff;
  padding: 0 10px 0 10px;
}
</style>
