<template>
  <div class="row">
    <div class="divider"></div>
    <MusicComp
      :song1="song1"
      :song2="song2"
      :song3="song3"
      :artist1="artist1"
      :artist2="artist2"
      :artist3="artist3"
    >
    </MusicComp>
  </div>
</template>

<script>
import  MusicComp  from "./Music.vue";
//theres a difference when import as {} and without it
export default {
  name: "MusicBar",
  components: { MusicComp },
  data() {
    return {
      song1: null,
      artist1: null,
      song2: null,
      artist2: null,
      song3: null,
      artist3: null,
    };
  },
  mounted() {
    //TODO: study this again, refactor where needed, hash api key
    const apiGetUrl = new URL(
      "https://ws.audioscrobbler.com/2.0/?method=user.getrecenttracks"
    );
    apiGetUrl.searchParams.append("user", "saresh22");
    apiGetUrl.searchParams.append("api_key", "21162143911dae90d1b2ed9e7098eec8");
    apiGetUrl.searchParams.append("format", "json");
    console.log(apiGetUrl.toString());
    fetch(apiGetUrl)
      .then((resp) => resp.json())
      .then((data) => {
        function removeDuplicates(arr) {
          const result = [];
          const duplicatedIndices = [];

          arr.forEach((current, index) => {
            if (duplicatedIndices.includes(index)) return;

            result.push(current);

            for (
              let comparisonIndex = index + 1;
              comparisonIndex < arr.length;
              comparisonIndex++
            ) {
              const comparison = arr[comparisonIndex];
              const currentKeys = Object.keys(current);
              const comparisonKeys = Object.keys(comparison);

              if (currentKeys.length !== comparisonKeys.length) {
                continue;
              }

              const currentKeysString = currentKeys.sort().join("").toLowerCase();
              const comparisonKeysString = comparisonKeys.sort().join("").toLowerCase();

              if (currentKeysString !== comparisonKeysString) {
                continue;
              }

              let valuesEqual = true;

              for (let i = 0; i < currentKeys.length; i++) {
                const key = currentKeys[i];
                if (current[key] !== comparison[key]) {
                  valuesEqual = false;
                  break;
                }
              }

              if (valuesEqual) {
                duplicatedIndices.push(comparisonIndex);
              }
            }
          });

          return result;
        }

        let res = data.recenttracks.track;
        let songs = [];
        for (let index = 0; index < res.length; index++) {
          //add song name: artistName to object
          let song = res[index].name;
          let artist = res[index].artist["#text"];
          let object = {
            song,
            artist,
          };

          songs.push(object);
        }

        let songStripped = removeDuplicates(songs);
        let firstThree = songStripped.slice(0, 3);
        console.log(firstThree);

        this.song1 = firstThree[0].song;
        this.song2 = firstThree[1].song;
        this.song3 = firstThree[2].song;

        this.artist1 = firstThree[0].artist;
        this.artist2 = firstThree[1].artist;
        this.artist3 = firstThree[2].artist;
      });
  },
};
</script>

<style scoped>
.row {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.divider {
  display: none;
  width: 100%;
  height: 3px;
  margin: 2rem 0;
}

@media screen and (max-width: 610px) {
  .divider {
    display: block;
    margin-top: -15px !important;
  }

  .row {
    flex-direction: column;
    margin-top: -40px !important;
  }
}
</style>
