<template>
  <div class="skill">
    <h2>Tech Stack 🛠</h2>
    <div class="items">
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">Java</div>
          <span
            ><font-awesome-icon class="fa-java fa-lg" icon="fa-brands fa-java"
          /></span>
        </div>
      </div>
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">Python</div>
          <span
            ><font-awesome-icon href="#" class="fa-python fa-lg" icon="fa-brands fa-python"
          /></span>
        </div>
      </div>
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">PHP</div>
          <span><font-awesome-icon class="fa-php fa-lg" icon="fa-brands fa-php" /></span>
        </div>
      </div>
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">SQL</div>
          <span
            ><font-awesome-icon class="fa-database fa-lg" icon="fa-solid fa-database"
          /></span>
        </div>
      </div>
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">HTML</div>
          <span
            ><font-awesome-icon class="fa-html5 fa-lg" icon="fa-brands fa-html5"
          /></span>
        </div>
      </div>
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">CSS</div>
          <span
            ><font-awesome-icon class="fa-css3-alt fa-lg" icon="fa-brands fa-css3-alt"
          /></span>
        </div>
      </div>
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">JavaScript</div>
          <span
            ><font-awesome-icon class="fa-js-square fa-lg" icon="fa-brands fa-js"
          /></span>
        </div>
      </div>
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">Amazon Web Services (AWS)</div>
          <span><font-awesome-icon class="fa-aws fa-lg" icon="fa-brands fa-aws" /></span>
        </div>
      </div>
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">Adobe Experience Manager (AEM)</div>
          <span>
            <img href="#" class="fa-aem fa-lg" src="../assets/img/logos/aem.svg" height="20" />
          </span>
        </div>
      </div>
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">Springboot</div>
          <span>
            <img href="#"
              class="fa-springboot fa-lg"
              src="../assets/img/logos/spring-boot.svg"
              height="20"
            />
          </span>
        </div>
      </div>
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">Vue.js</div>
          <span
            ><font-awesome-icon class="fa-vuejs fa-lg" icon="fa-brands fa-vuejs"
          /></span>
        </div>
      </div>
      <div class="wrapper">
        <div class="icon logo">
          <div class="tooltip">Linux OS</div>
          <span
            ><font-awesome-icon class="fa-linux fa-lg" icon="fa-brands fa-linux"
          /></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SkillsComp",
};
</script>

<style scoped>
h2 {
  font-weight: 500;
  color: white;
  font-size: 1.8rem;
  border-bottom: 10px solid green;
  line-height: 0.4;
  width: 100px;
  transition: all ease 0.3s;
  white-space: nowrap;
}

h2:hover {
  font-size: 1.8rem;
  font-weight: 500;
  color: white;
  border-bottom: 10px solid #1db954;
  line-height: 0.4;
  width: 210px;
  transition: 0.5s;
}

span {
  padding: 20px;
}

.wrapper {
  display: inline-flex;
  vertical-align: center;
}

.wrapper .icon {
  margin: 0 10px;
  text-align: center;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  position: relative;
  z-index: 2;
  transition: 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.wrapper .icon span {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 60px;
  width: 60px;
  margin-bottom: 1em;
  background-color: #1d2430;
  border-radius: 50%;
  position: relative;
  z-index: 2;
  box-shadow: 0px 10px 10px rgba(0, 0, 0, 0.1);
  transition: 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.wrapper .icon span i {
  line-height: 60px;
  font-size: 25px;
}

.wrapper .icon .tooltip {
  position: absolute;
  top: 0;
  z-index: 1;
  background: #fff;
  color: #fff;
  padding: 10px 18px;
  font-size: 20px;
  font-weight: 500;
  border-radius: 25px;
  opacity: 0;
  pointer-events: none;
  box-shadow: 0px 10px 10px rgba(0, 0, 0, 0.1);
  transition: 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
  white-space: nowrap;
}

.wrapper .icon:hover .tooltip {
  top: -70px;
  opacity: 1;
  pointer-events: auto;
  white-space: nowrap;
}

.fa-python {
  color: #fff;
}

.fa-vuejs {
  color: #fff;
}

.fa-html5 {
  color: #fff;
}

.fa-js-square {
  color: #fff;
}

.fa-java {
  color: #fff;
}

.fa-springboot {
  color: #fff;
}

.fa-aem {
  color: #fff;
}

.fa-css3-alt {
  color: #fff;
}

.fa-database {
  color: #fff;
}

.fa-linux {
  color: #fff;
}

.fa-php {
  color: #fff;
}

.fa-aws {
  color: #fff;
}

.icon .tooltip::before {
  position: absolute;
  content: "";
  height: 15px;
  width: 15px;
  background: #fff;
  left: 50%;
  bottom: -6px;
  transform: translateX(-50%) rotate(45deg);
  transition: 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.wrapper .icon:hover span {
  color: #fff;
}

.wrapper .icon:hover span,
.wrapper .icon:hover .tooltip {
  text-shadow: 0px -1px 0px rgba(255, 255, 255, 0.5);
}

.wrapper .logo:hover span,
.wrapper .logo:hover .tooltip,
.wrapper .logo:hover .tooltip::before {
  background: #18d26e;
}

.items {
  margin: auto 0;
  display: flex;
  align-content: center;
  justify-content: center;
}

@media screen and (max-width: 1258px) {
  .items {
    width: 100%;
    display: block;
  }
}
@media screen and (max-width: 530px) {
  .items {
    width: 100%;
    display: block;
    justify-content: center;
    align-content: center;
  }
}
</style>
