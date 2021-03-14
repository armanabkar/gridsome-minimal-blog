<template>
  <div>
    <img
      src="https://qwizzeria.com/wp-content/uploads/2017/09/Lorem-ipsum.png"
      alt="Lorem Ipsum"
    />
    <p>
      Hi, I'm
      <strong>Lorem Ipsum</strong>, a Software Developer from Earth, Milky Way.
      You can follow me on
      <a href="/#" target="_blank">Twitter</a>
      or
      <a href="/#" target="_blank">Instagram</a>, see some of my work on
      <a href="/#" target="_blank">GitHub</a>, or read more about me on
      <a href="/#" target="_blank">LinkedIn</a>. <br />
      Please feel free to reach me at
      <a href="/#">loremipsum@gmail.com</a>.
    </p>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
div {
  align-items: center;
  display: flex;
  border: 2px dashed var(--border-color);
  border-radius: 8px;
  padding: 0 0.5rem;
  margin: 4rem 0 -4.5rem 0;
}

img {
  width: 7.5rem;
  height: 7.5rem;
  border-radius: 8px;
  /* border: 3px solid var(--primary); */
  margin-right: 0.7rem;
  margin-bottom: 0.1rem;
}

@media only screen and (max-width: 768px) {
  img {
    display: none;
  }
  div {
    text-align: center;
  }
}

p {
  font-size: 1.125rem;
}

strong {
  letter-spacing: 0.05rem;
  color: var(--border-color);
}

a {
  color: var(--text-color);
  text-decoration: none;
  box-shadow: inset 0 -0.12em 0 var(--border-color);
  -webkit-transition: box-shadow 0.2s ease-in-out, color 0.2s ease-in-out;
  transition: box-shadow 0.2s ease-in-out, color 0.2s ease-in-out;
}
a:hover {
  box-shadow: inset 0 -1.5em 0 var(--border-color);
  color: var(--bkg-color);
}
</style>