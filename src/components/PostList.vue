<template>
  <div class="post-list">
    <hr class="line" />
    <p class="date" v-html="post.date" />
    <g-link :to="post.path" class="post">
      <h3 class="title" v-html="post.title" />
    </g-link>
    <p class="description" v-html="post.description" />
    <div class="info">
      <b>{{ post.timeToRead }} min read</b> &nbsp;
      <g-link :to="post.path" class="read"
        >Read More ...
        <span class="visuallyhidden">about {{ post.title }}</span></g-link
      >
    </div>
  </div>
</template>

<script>
export default {
  props: ["post"],
}
</script>

<style>
.post {
  text-decoration: none;
  color: inherit;
  cursor: default;
}
.line {
  background-image: linear-gradient(
    to right,
    #aaaaaa05,
    var(--border-color),
    #aaaaaa05
  );
  border: 0;
  height: 2px;
  margin: 40px auto;
}

.title {
  font-size: 1.3rem;
  letter-spacing: 0.03rem;
}

.date {
  font-weight: 300;
  font-size: 0.9rem;
  font-style: italic;
}

.info {
  display: flex;
  justify-content: space-between;
}

.read {
  font-weight: bold;
  color: var(--border-color);
  text-decoration: none;
}
.read:hover {
  color: var(--text-color);
}

.visuallyhidden {
  position: absolute !important;
  width: 1px;
  height: 1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  clip-path: inset(50%);
  border: 0;
}
.visuallyhidden:focus {
  display: inline-block;
  padding: 15px 23px 14px;
  width: auto;
  height: auto;
  clip: auto;
  color: var(--text-color);
  background-color: var(--bkg-color);
  clip-path: unset;
}
</style>
