<template>
  <div>
    <h2>Music 🎼</h2>
    <p>My most recently played music tracks are:</p>
    <ul>
      <li>
        {{ song1 }} —
        <span class="italics">{{ artist1 }}</span>
      </li>
      <li>
        {{ song2 }} —
        <span class="italics">{{ artist2 }}</span>
      </li>
      <li>
        {{ song3 }} —
        <span class="italics">{{ artist3 }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MusicComp",
  props: {
    song1: String,
    song2: String,
    song3: String,
    artist1: String,
    artist2: String,
    artist3: String,
  },
};
</script>

<style scoped>
@counter-style repeating-emoji {
  system: cyclic;
  symbols: "🗿" "🪐" "🌌";
  suffix: " ";
  height: auto;
  width: 100px;
}

div {
  width: 100%;
}

h2 {
  font-size: 1.8rem;
  font-weight: 500;
  color: white;
  border-bottom: 10px solid green;
  line-height: 0.4;
  width: 55px;
  transition: all ease 0.3s;
  white-space: nowrap;
}

h2:hover {
  font-size: 1.8rem;
  font-weight: 500;
  color: white;
  border-bottom: 10px solid #1db954;
  line-height: 0.4;
  width: 150px;
  transition: 0.5s;
  white-space: nowrap;
}

p {
  color: white;
  font-weight: 300;
  font-size: 1rem;
  line-height: 20px;
}

ul {
  color: white;
  margin-block-start: 0;
  padding-inline-start: 20px;
  margin-left: 10px;
  list-style-type: repeating-emoji;
  margin-block-end: 0;
}

li {
  line-height: 1.3;
  padding-bottom: 4px;
}

@media screen and (max-width: 610px) {
  div {
    width: 100%;
  }

  .italics {
    font-style: italic;
  }
}
</style>
