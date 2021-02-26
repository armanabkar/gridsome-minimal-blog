<template>
  <main class="layout" role="main">
    <Header />
    <slot />
    <div class="footer">
      <p>
        Built with
        <a class="link" href="//gridsome.org">Gridsome</a>
        & Made with ❤️ by
        <a class="link" href="https://armanabkar.ir/">Arman Abkar</a>
      </p>
    </div>
  </main>
</template>

<script>
import Header from "./partials/Header"
export default {
  components: {
    Header,
  },
}
</script>

<style>
:root {
  --text-color: #3b3936;
  --border-color: #2196f3;
  --bkg-color: #fafafa;
  --line-color: #2196f3;
}
:root [data-theme="sepia"] {
  --text-color: #433422;
  --border-color: #a97c5d;
  --bkg-color: #f1e7d0;
  --line-color: #a97c5d;
}
:root [data-theme="dark"] {
  --text-color: #eeeeee;
  --border-color: #52596e;
  --bkg-color: #252525;
  --line-color: #52596e;
}
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
  border-top: 0.7rem solid var(--border-color);
  border-bottom: 0.7rem solid var(--border-color);
  border-left: 0.7rem solid var(--border-color);
  min-height: 100vh;
  background-color: var(--bkg-color);
  color: var(--text-color);
  transition: background 0.3s;
}

.layout {
  max-width: 800px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.footer {
  padding-top: calc(30em / 4);
  text-align: center;
  font-size: 1em;
}

a {
  color: var(--border-color);
  text-decoration: none;
}

.link {
  font-weight: bold;
  color: var(--border-color);
  text-decoration: none;
}
.link:hover {
  color: var(--text-color);
}

code {
  font-family: "SF Mono", menlo, inconsolata, monospace;
  font-size: calc(1em - 2px);
  font-weight: 600;
  padding: 0.2em 0.4em;
  border-radius: 2px;
  color: var(--bkg-color);
  background-color: var(--text-color);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

pre {
  border-radius: 8px !important;
  margin: 1em 0 !important;
}

pre code {
  padding: 0;
  background-color: inherit;
  font-size: 1rem !important;
}

img {
  max-width: 80%;
}

::-webkit-scrollbar {
  width: 0.7rem; /* width of the entire scrollbar */
  overflow: auto;
}

::-webkit-scrollbar-track {
  background: var(--bkg-color); /* color of the tracking area */
}

::-webkit-scrollbar-thumb {
  background-color: var(--border-color); /* color of the scroll thumb */
}
</style>
