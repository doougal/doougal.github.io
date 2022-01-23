<template>
  <div>
    <header>
      <img id="profilePhoto" alt="Profile Photo" src="./assets/headshot-circle.png" />

      <h1>Alex Burling</h1>
      <p>Associate DevOps Engineer @ MYOB</p>
      <p>System Developer @ Gaia Healthcare NZ</p>
    </header>

    <div id="links">
      <div class="link">
        <Icon icon="clarity:phone-handset-solid" /> Contact
        <div class="arrows" v-on:click="clicked('contact')">
          <Icon icon="akar-icons:chevron-down" v-if="!isClicked.contact" />
          <Icon icon="akar-icons:chevron-up" v-if="isClicked.contact" />
        </div>

        <div v-show="isClicked.contact">
          <p>+64 021 084 57732</p>
          <a href="mailto:burling_alex@yahoo.com">burling_alex@yahoo.com</a>
          <p>Christchurch, New Zealand</p>
        </div>
      </div>

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

      <!-- <div class="link">
        <div :class="{ active: isClicked.cybersec }">
          <Icon icon="simple-icons:hackthebox" /> Cyber Security
          <div class="arrows" v-on:click="clicked('cybersec')">
            <Icon icon="akar-icons:chevron-down" v-if="!isClicked.cybersec" />
            <Icon icon="akar-icons:chevron-up" v-if="isClicked.cybersec" />
          </div>
        </div>
        <div v-if="isClicked.cybersec">
          <a
            class="link sublink"
            href="https://app.hackthebox.eu/users/779571"
            target="_blank"
            rel="noopener"
            ><Icon icon="simple-icons:hackthebox" /> HackTheBox</a
          >

          <a
            class="link sublink"
            href="https://tryhackme.com/p/doog"
            target="_blank"
            rel="noopener"
            ><Icon icon="simple-icons:tryhackme" /> TryHackMe</a
          >

          <a
            class="link sublink"
            href="https://www.hackerrank.com/burling_alex"
            target="_blank"
            rel="noopener"
            ><Icon icon="fa-brands:hackerrank" /> HackerRank</a
          >
        </div>
      </div> -->
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
  data() {
    return {
      isClicked: { contact: false, cybersec: false },
    };
  },
  methods: {
    clicked(link) {
      this.isClicked[link] = this.isClicked[link] ? false : true;
    },
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
  user-select: none;
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
  overflow-x: hidden;
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
  min-width: 250px;
}

.sublink {
  min-width: 200px;
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

.arrows {
  float: right;
  cursor: pointer;
}

a {
  color: inherit;
}

.active {
  margin-bottom: 20px;
}
</style>
