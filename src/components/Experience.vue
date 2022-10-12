<template>
  <div>
    <h2>Experience ⚛</h2>
    <div class="timeline">
      <div class="year-container">
        <span class="year">2022</span>
      </div>
      <ul>
        <br>
        <li>
          <div class="content">
            <a href="https://www.growthops.asia/" target="_blank">
              <h3>GrowthOps Asia</h3>
              <h5>Java Developer</h5>
              <div class="grey">Jul 2021 — Present</div>
              <br>
              <p>
                - Development and website enhancements of multiple clients from Australia,
                China, Indonesia, Thailand, Vietnam, Singapore and Malaysia using Adobe Experience
                Manager (AEM)
                <br>
                - Actively involved in projects and responding to business users on bug
                fixes and enhancements
                <br>
                - Required proper understanding of clients business domain as well
                as the complex AEM framework and the tech surrounding it
              </p>
            </a>
          </div>
        </li>
      </ul>
    </div>
    <div class="timeline">
      <div class="year-container">
        <span class="year">2020</span>
      </div>
      <ul>
        <br>
        <li>
          <div class="content">
            <a href="https://senwave.com.my/" target="_blank">
              <h3>Senwave Retail Solutions</h3>
              <h5>Software Developer</h5>
              <div class="grey">Oct 2020 —  Jul 2021</div>
              <br>
              <p>
                - Developed microservices using Java & Spring Boot to create RESTful endpoints for 
                data processing with Magento/Adobe Commerce
                <br>
                - REST endpoints involve CRUD operations in a huge Postgres Data Lake
              </p>
            </a>
          </div>
        </li>
      </ul>
    </div>
    <div class="timeline">
      <div class="year-container">
        <span class="year">2018</span>
      </div>
      <ul>
        <br />
        <li>
          <div class="content">
            <a href="https://juristech.net/juristech/" target="_blank">
              <h3>JurisTech</h3>
              <h5>Software Engineer</h5>
              <div class="grey">Sep 2018 —  Apr 2019</div>
              <br>
              <p>
                - Actively assisted developers in development of features as an intern
                <br>
                - Developed database scripts using Oracle's PL/SQL as well as managing the database
                <br>
                - Awarded intern distinction for outstanding commitment towards project and team members
              </p>
            </a>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "ExperienceComp",
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
  margin-bottom: 2rem;
  white-space: nowrap;
}

strong {
  font-weight: 500;
  color: #1db954;
}

a {
  color: white;
  border: none;
  text-decoration: none;
}

.green-dot {
  width: 16px;
  height: 16px;
  background: #1db954;
  border-radius: 50%;
  margin-left: -0.45em;
}

.year-container {
  position: absolute;
  margin: 0 -2.25em;
  z-index: 9999;
}

.year {
  color: white;
  font-weight: 500;
  font-size: 1.5rem;
  background: #1db954;
  border-radius: 16px;
  padding: 0.5rem;
}

h2:hover {
  font-size: 1.8rem;
  font-weight: 500;
  color: white;
  border-bottom: 10px solid #1db954;
  line-height: 0.4;
  width: 200px;
  transition: all ease 0.3s;
  white-space: nowrap;
}

div {
  color: white;
  font-family: "Poppins", sans-serif !important;
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
  perspective: 800px;
}

.grey {
  color: #ddd;
  font-size: 0.9rem;
}

body {
  display: flex;
}

.timeline {
  width: 100%;
  background-color: #1a202c;
  color: #fff;
  /* padding: 30px 20px; */
  word-wrap: normal;
  margin-left: 15px;
}

.timeline ul {
  list-style-type: none;
  border-left: 2px solid white;
  padding: 10px 5px;
}

.timeline ul li {
  padding: 8px 20px;
  position: relative;
  cursor: pointer;
  transition: 0.5s;
}

.timeline ul li span {
  display: inline-block;
  border-radius: 25px;
  padding: 2px 5px;
  font-size: 15px;
  text-align: center;
}

.timeline ul li .content h3 {
  color: #1db954;
  font-size: 1.6rem;
  padding-top: 5px;
  font-weight: 500;
  margin-bottom: 0.2rem;
}

h5 {
  font-size: 1.2rem;
  padding-top: 5px;
  font-weight: 500;
  margin-bottom: 8px;
}

.timeline ul li content p {
  padding: 5px 0px 15px 0px;
  font-size: 15px;
}

.timeline ul li::before {
  position: absolute;
  content: "";
  width: 10px;
  height: 10px;
  background-color: lawngreen;
  border-radius: 50%;
  left: -11px;
  top: 28px;
  transition: 0.5s;
  margin: 0;
}

.timeline ul li:hover {
  background-color: #1b405e;
  border-radius: 8px;
}

.timeline ul li:hover::before {
  background-color: #0f0;
  box-shadow: 0px 0px 10px 2px #0f0;
}

@media (max-width: 300px) {
  .timeline {
    width: 100%;
    padding: 30px 5px 30px 10px;
  }

  .timeline ul li .content h3 {
    color: #1db954;
    font-size: 15px;
  }
}
</style>
