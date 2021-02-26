<template>
  <Layout>
    <div class="post-title">
      <h1>{{ $page.post.title }}</h1>
      <p class="post-date">
        {{ $page.post.date }} | {{ $page.post.timeToRead }} min read
      </p>
    </div>
    <div class="post-content">
      <p v-html="$page.post.content" />
    </div>
    <Bio />
  </Layout>
</template>

<page-query>
query Post ($path: String!) {
   post: post (path: $path) {
    id
    title
    content
    date (format: "D MMMM YYYY")
    timeToRead
  }
}
</page-query>

<script>
import Bio from "@/components/Bio";
export default {
  components: {
    Bio,
  },
  metaInfo() {
    return {
      title: this.$page.post.title,
    };
  },
};
</script>

<style>
.post-title {
  text-align: center;
  font-size: 30px;
  line-height: 0.8em;
  padding: 1.5em 0 0.7em 0;
  font-family: "Stylish";
}

.post-date {
  font-size: 16px;
  font-weight: 400;
}

.post-content {
  font-size: 1.185rem;
}
</style>
