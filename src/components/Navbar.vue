<template>
  <nav>
    <div class="name" id="name">
      <h1>Hari Saresh</h1>
    </div>
    <br>
    <ul>
      <a href="https://www.linkedin.com/in/hari-saresh-040b92187/" target="_blank" rel="noopener noreferrer">
        <li class="'last'">
          <font-awesome-icon class="fa-linkedin fa-lg" icon="fab fa-linkedin " />
        </li>
      </a>
      <a href="https://github.com/theBlackParade22" target="_blank" rel="noopener noreferrer">
        <li>
          <font-awesome-icon class="fa-github fa-lg" icon="fab fa-github" />
        </li>
      </a>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavbarComp"
};
</script>

<!-- "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-top: 10px;
}

.name {
  display: flex;
  align-items: flex-end;
  white-space: nowrap;
}

.name h1 {
  margin: 0 0 0 0;
  font-size: 3.2rem;
  font-weight: 600;
  border-bottom: 6px solid #18D26E;
  line-height: 0.6;
  font-family: 'Dancing Script', cursive;
  width: auto;
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
  background-color: #18D26E;
  transform: translateY(-5px);
  transition: all ease 0.2s;
}

.fa-github {
  color: #fff;
}

.fa-linkedin {
  color: #fff;
}

@media screen and (max-width: 1250px) {
  ul {
    justify-content: flex-start;
    align-items: flex-start;
    padding-inline-start: 0;
    margin-top: 2rem;
  }

  li {
    margin-left: 0;
    margin-right: 1rem;
  }

  .first {
    margin-right: 1rem;
    margin-left: 0;
  }

  .last {
    margin: 0;
  }
}

@media screen and (max-width: 570px) {
  ul {
    width: 100%;
  }

  li {
    margin-left: 0;
    margin-right: 1rem;
  }

  .first {
    margin-right: 1rem;
    margin-left: 0;
  }

  .last {
    margin: 0;
  }
}

@media screen and (max-width: 410px) {
  li {
    margin-right: 0.5rem;
  }

  .first {
    margin-right: 0.5rem;
    margin-left: 0;
  }

  .last {
    margin: 0;
  }

  font-awesome-icon {
    height: 80%;
  }
}
</style>