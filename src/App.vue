<template>
  <div>
    <header>
      <img id="profilePhoto" alt="Profile Photo" src="./assets/profile.png" />

      <h1>Alex Burling</h1>
      <p>System Developer @ Gaia Healthcare NZ</p>
      <p>BSC Computer Science @ University of Canterbury</p>
    </header>

    <div id="links">
      <a
        class="link"
        href="https://github.com/doougal"
        target="_blank"
        rel="noopener"
        ><Icon icon="akar-icons:github-fill" /> GitHub</a
      >
      <a
        class="link"
        href="https://www.linkedin.com/in/alex-burling/"
        target="_blank"
        rel="noopener"
        ><Icon icon="akar-icons:linkedin-fill" /> LinkedIn</a
      >
      <a
        class="link"
        href="https://app.hackthebox.eu/users/779571"
        target="_blank"
        rel="noopener"
        ><Icon icon="simple-icons:hackthebox" /> HackTheBox</a
      >
      <a
        class="link"
        href="https://tryhackme.com/p/doog"
        target="_blank"
        rel="noopener"
        ><Icon icon="simple-icons:tryhackme" /> TryHackMe</a
      >
      <a
        class="link"
        href="https://www.hackerrank.com/burling_alex"
        target="_blank"
        rel="noopener"
        ><Icon icon="fa-brands:hackerrank" /> HackerRank</a
      >
    </div>

    <footer>
      <a
        id="footerLink"
        href="https://github.com/doougal/doougal.github.io"
        target="_blank"
        rel="noopener"
        >See the code for this site</a
      >
    </footer>
  </div>
</template>

<script>
import { Icon } from "@iconify/vue";

export default {
  name: "App",
  components: {
    Icon,
  },
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

#footerLink {
  display: block;
  margin-bottom: 20px;
  padding: 17px;
  font-size: 1rem;
  font-weight: 500;
  text-align: center;
  text-decoration: none;
  color: var(--color);
}
</style>
