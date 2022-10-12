<template>
  <div class="hero">
    <div class="image-holder">
      <img src="../assets/img/me.jpg" alt="Image of Hari Saresh" />
    </div>
    <div class="text">
      <div class="top-text">
        <h2>Hi, I'm Hari! 🙏🏾</h2>
        <h3>
          I'm a
          <span>
            <!-- shit does not work in Vue3 -->
            <VueTyper
              :text="['Software Engineer', 'Software Developer', 'Java Developer']"
              :repeat="Infinity"
              :shuffle="false"
              initial-action="typing"
              :pre-type-delay="70"
              :type-delay="70"
              :pre-erase-delay="2000"
              :erase-delay="250"
              erase-style="select-all"
              :erase-on-complete="true"
              care-animation="blink"
            >
            </VueTyper>
          </span>
          from <br />
          Kuala Lumpur.
        </h3>
      </div>
      <div class="bottom-text">
        <p class="b-margin">
          I graduated with a bachelors degree in IT (HONS) with a major in Software
          Engineering at
          <a
            target="_blank"
            rel="noopener noreferrer"
            class="green"
            href="https://www.utp.edu.my/Pages/Home.aspx"
            >PETRONAS University of Technology</a
          >
          in 2020.
          <br /><br />
          My development experience includes loan origination, retail management and
          content management systems/frameworks. I started of with a background in Backend
          development and have been refining my Frontend skills gradually. I enjoy
          learning and utilizing new tech on the job. 👨🏾‍💻
        </p>
        <p>
          My favourite hobbies include running 🏃🏾‍♂️, playing football ⚽ and reading 📚.
        </p>
      </div>
      <div class="contact">
        <a href="#contact">
          <div class="contact-me">Contact Me 📲</div>
        </a>
      </div>
      <!-- TODO: fix `here` href to #projects -->
      <p class="center">
        Check out my expertise<a
          rel="noopener noreferrer"
          class="green"
          href="#experience"
          style="padding-top: 1px; margin-left: 5px; margin-right: 1px"
          >here</a
        >.
      </p>
    </div>
  </div>
</template>

<script>
import { VueTyper } from "vue-typer";

export default {
  name: "HeroComp",
  components: {
    VueTyper,
  },
};
</script>

<!-- "scoped" attribute to limit CSS to this component only -->
<style scoped>
::v-deep .typed {
  color: lawngreen !important;
}
::v-deep .custom.caret {
  background-color: green !important;
}

.bottom-text {
  text-align: justify;
}

ul {
  margin: 0;
  list-style-type: none;
  display: flex;
  flex-direction: row;
}

li {
  margin-left: 2rem;
  padding: 10px;
  display: flex;
  border-radius: 8px;
  justify-content: center;
  align-items: center;
  background-color: #1b405e;
  transition: all ease 0.2s;
}

li:hover {
  background-color: #18d26e;
  transform: translateY(-5px);
  transition: all ease 0.2s;
}

/* may need to check source code */
.green {
  color: #18d26e;
  text-decoration: none;
  font-weight: bold;
  margin: 5px;
  /* transition: siz; */
}

.green:hover {
  color: lawngreen;
  text-decoration: none;
  font-weight: bolder;
  margin: 5px;
  /* transition: siz; */
}

.center {
  text-align: center;
  margin-top: 5px;
}

img {
  height: 200px;
  border-radius: 8px;
}

.b-margin {
  margin-bottom: 1rem;
}

.image-holder {
  margin-top: 20px;
  height: 125px;
}

.hero {
  display: flex;
  margin-bottom: -2.5rem;
}

.text {
  height: 500px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  color: white;
  margin-left: 2rem;
  margin-bottom: 2rem;
}

a {
  text-decoration: none;
}

.contact {
  margin-top: 2rem;
}

.contact-me {
  font-size: 1.1rem;
  font-weight: 500;
  background-color: #18d26e;
  color: white;
  border-radius: 8px;
  text-align: center;
  padding: 10px;
  vertical-align: center;
  transition: all ease 0.3s;
}

.contact-me:hover {
  transform: translateY(-5px);
  transition: all ease 0.2s;
}

h2,
p {
  margin: 0;
}

h2 {
  font-weight: 500;
  font-size: 1.8rem;
}

h3 {
  font-weight: 480;
  font-size: 1.4rem;
  height: 85px;
}

p {
  font-weight: 300;
  font-size: 1rem;
  line-height: 1.3;
}

@media screen and (max-width: 570px) {
  ul {
    margin-left: 10px;
  }
}

@media screen and (max-width: 1258px) {
  .hero {
    flex-direction: column;
    margin-bottom: 0rem;
  }

  img {
    height: 150px;
    width: auto;
    clip-path: circle(700px at center);
    position: relative;
    top: -20px;
    margin: 0;
  }

  .text {
    margin-left: 0;
    height: auto;
    margin-bottom: -0.5rem;
  }

  h2 {
    margin-bottom: 1rem;
    margin-top: 1rem;
  }

  li {
    margin-right: 0.5rem;
    margin-left: 0.5rem;
  }

  .contact {
    margin-top: 16px;
  }
}
</style>
