<template>
  <Layout>
    <header class="header">
      <h1 v-html="$page.metadata.siteName" />
      <h2 v-html="$page.metadata.siteDescription" />
    </header>
    <section class="posts">
      <PostList
        v-for="edge in $page.allPost.edges"
        :key="edge.node.id"
        :post="edge.node"
      />
    </section>
  </Layout>
</template>

<script>
import PostList from "@/components/PostList"
export default {
  components: {
    PostList,
  },
  metaInfo: {
    title: "Gridsome Blog",
  },
}
</script>

<page-query>
query {
  metadata {
    siteName
    siteDescription
  }
  allPost {
    totalCount
    edges {
      node {
        id
        title
        timeToRead
        description
        date (format: "D MMMM YYYY")
        path
      }
    }

  }
}
</page-query>

<style>
.header {
  font-family: "Stylish";
  font-size: 35px;
  text-align: center;
  line-height: 1em;
  padding: 0.8em;
}

.header h2 {
  font-weight: 200;
  font-size: 35px;
}

@media only screen and (max-width: 992px) {
  .header {
    font-family: "Stylish";
    font-size: 2.1em;
    text-align: center;
    line-height: 2em;
    padding: 0.15em;
  }

  .header h2 {
    font-weight: 200;
    font-size: 0.9em;
    line-height: 1.5em;
  }
}
</style>
