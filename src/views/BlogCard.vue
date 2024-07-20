<template>
  <div class="blog-card">
    <h2>{{ post.title }}</h2>
    <p>{{ post.body.substring(0, 100) }}...</p>
    <button>Read More</button>
  </div>
</template>

<script>
export default {
  name: "BlogCard",
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.blog-card {
  border: 1px solid #ddd;
  padding: 16px;
  border-radius: 8px;
  cursor: pointer;
  transition: background 0.3s;
  flex: 1 1 calc(33% - 16px);
  box-sizing: border-box;
}
.blog-card:hover {
  background: #f0f0f0;
  color: black;
}
.blog-card h2 {
  font-size: 1.5em;
}
.blog-card button {
  background: rgba(82, 5, 123, 0.7);
  border-radius: 5px;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 4px;
  cursor: pointer;
  margin-top: 10px;
}
</style>
