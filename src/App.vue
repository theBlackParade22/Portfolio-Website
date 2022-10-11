<script>
import NavbarComp from "./components/Navbar.vue";
import HorizontalDivider from "./components/HorizontalDivider.vue";
import HeroComp from "./components/Hero.vue";
import SkillsComp from "./components/Skills.vue";
import ExperienceComp from "./components/Experience.vue";
import MusicBar from "./components/MusicBar.vue";
import ContactComp from "./components/Contact.vue";
import FooterComp from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    NavbarComp,
    HorizontalDivider,
    HeroComp,
    SkillsComp,
    ExperienceComp,
    MusicBar,
    ContactComp,
    FooterComp,
  },
  methods: {
    scrollToTop() {
      window.scrollTo({ top: 0, left: 0, behavior: "smooth" });
    },
  },
};
</script>

<template>
  <div id="app">
    <!-- <cursor-fx color="lawngreen"></cursor-fx> -->
    <div class="home">
      <div>
        <button class="scroll-top" v-on:click="scrollToTop()">
          <font-awesome-icon id="scroll-top" class="fa-lg" icon="fa-solid fa-chevron-up" />
        </button>
      </div>
      <NavbarComp></NavbarComp>
      <HorizontalDivider></HorizontalDivider>
      <HeroComp></HeroComp>
      <HorizontalDivider></HorizontalDivider>
      <SkillsComp></SkillsComp>
      <HorizontalDivider></HorizontalDivider>
      <a name="experience"></a>
      <ExperienceComp></ExperienceComp>
      <HorizontalDivider></HorizontalDivider>
      <MusicBar></MusicBar>
      <HorizontalDivider></HorizontalDivider>
      <a name="contact"></a>
      <ContactComp></ContactComp>
      <HorizontalDivider></HorizontalDivider>
      <FooterComp></FooterComp>
    </div>
  </div>
</template>

<style>
* {
  box-sizing: border-box;
}

html {
  padding: 0;
  margin: 0;
}

body {
  background-color: #1a202c;
  font-family: "Poppins", sans-serif;
  overflow-x: hidden;
}

::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #2c3649;
  border-radius: 0.5rem;
}

::-webkit-scrollbar-thumb {
  background: #1db954;
  border-radius: 0.5rem;
}

::-webkit-scrollbar-thumb:hover {
  background: lawngreen;
}

.scroll-top {
  position: fixed;
  bottom: 15%;
  left: 85%;
  background-color: #1db954;
  border: none;
  margin-left: 2rem;
  padding: 10px;
  display: flex;
  border-radius: 8px;
  justify-content: center;
  align-items: center;
  transition: all ease 0.2s;
  z-index: 2;
}

.scroll-top:hover {
  transform: scale(1.2);
  transition: 0.5s;
  color: white;
}

.home {
  max-width: 870px;
  margin: 2rem auto;
}

@media screen and (max-width: 1500px) {
  .home {
    margin: 2rem 20rem;
  }
}

@media screen and (max-width: 1380px) {
  .home {
    margin: 2rem 15rem;
  }
}

@media screen and (max-width: 936px) {
  .home {
    margin: 2rem;
  }

  .scroll-top {
    visibility: hidden;
  }
}

@media screen and (max-width: 320px) {
  .home {
    margin: 2rem 1rem;
  }
}
</style>
