<template>
  <div class="blog-list-container">
    <h1 class="header">Blogs</h1>
    <div  class="blog-list">
      <BlogCard v-for="post in posts" :key="post.id" :post="post"  />
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import BlogCard from './BlogCard.vue';

export default {
  name: 'Blogs',
  components: {
    BlogCard,
  },
  data() {
    return {
      posts: [],
    };
  },
  mounted() {
    this.fetchData();
  },
  methods: {
    async fetchData() {
      try {
        const response = await axios.get('https://jsonplaceholder.typicode.com/posts');
        this.posts = response.data;
      } catch (error) {
        this.error = 'Data Failed';
      }
    },

  },
};
</script>

<style scoped>
.blog-list-container {
  padding: 40px;
padding-top:100px ;
  margin: 0 auto;
  color: aliceblue;
background: var(--background, #000);
  font-family: poppins;
  }

.header {
  text-align: center;
  margin-bottom: 20px;
}

.loading, .error {
  text-align: center;
}

.blog-list {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
}
</style>
