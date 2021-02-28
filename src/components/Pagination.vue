<template>
  <section>
    <nav role="navigation" aria-label="pagination" class="pagination">
      <span v-if="info.isFirst"></span>
      <span v-if="!info.isFirst">
        <g-link
          :to="previousPage(info.currentPage)"
          :rel="info.currentPage == 1 ? 'nofollow' : 'prev'"
          class="link"
        >
          &larr; Previous Page
        </g-link>
      </span>
      <span v-if="!info.isLast">
        <g-link
          :to="nextPage(info.currentPage, info.totalPages)"
          :rel="info.currentPage == info.totalPages ? 'nofollow' : 'next'"
          class="link"
        >
          Next Page &rarr;
        </g-link>
      </span>
      <span v-if="info.isLast"></span>
    </nav>
  </section>
</template>

<script>
export default {
  props: ["base", "info"],
  methods: {
    previousPage(currentPage) {
      return [0, 1].includes(currentPage - 1)
        ? `${this.basePath}/`
        : `${this.basePath}/${currentPage - 1}/`
    },
    nextPage(currentPage, totalPages) {
      return totalPages > currentPage
        ? `${this.basePath}/${currentPage + 1}/`
        : `${this.basePath}/${currentPage}/`
    },
  },
  computed: {
    basePath() {
      return this.base || ""
    },
  },
}
</script>

<style scoped>
.pagination {
  font-family: "Stylish";
  font-weight: bold;
  font-size: 1.3rem;
  display: flex;
  justify-content: space-between;
  margin: 2.9rem auto -4.7rem auto;
}
</style>