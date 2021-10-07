<template>
  <div>
    
    <header>
      <img id="profilePhoto" alt="Profile Photo" src="./assets/profile.png" />

      <h1>Alex Burling</h1>
      <p>Software Developer</p>
    </header>

    <div id="links">
      <a
        class="link"
        href="https://github.com/doougal"
        target="_blank"
        rel="noopener"
        >GitHub</a
      >
      <a
        class="link"
        href="https://www.linkedin.com/in/alex-burling/"
        target="_blank"
        rel="noopener"
        >LinkedIn</a
      >
    </div>

    <footer>I made this website myself</footer>

  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
@import "../node_modules/typeface-roboto/index.css";

:root {
  --font: "Roboto Mono", monospace;
  --background: #202124;
  --color: #979ba7;
}

#app {
  font-family: var(--font);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--color);
  margin-top: 30px;
}

body {
  background-color: var(--background);
  margin: 0;
  padding: 0;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  display: flex;
  min-height: 100vh;
  min-width: 100vw;
  flex-direction: column;
}

#profilePhoto {
  width: 150px;
  height: 150px;
  display: block;
  margin: 35px auto 20px;
  border-radius: 50%;
  border: solid var(--color) 3px;
}

#links {
  max-width: 90%;
  width: auto;
  display: inline-block;
  margin: 30px auto;
}

.link {
  display: block;
  margin-bottom: 20px;
  padding: 17px;
  font-size: 1rem;
  font-weight: 500;
  border-radius: 5px;
  border: dashed var(--color) 2px;
  text-align: center;
  text-decoration: none;
  color: var(--color);
}
</style>
