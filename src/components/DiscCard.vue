<template>
  <li class="col">
    <div class="content p-3 text-center">
      <img :src="imgUrl" :alt="songName" class="img-fluid mb-3">
      <h3 class="song-name mb-4">{{ songName }}</h3>
      <div class="artist">{{ artist }}</div>
      <div class="year">{{ year }}</div>
    </div>
  </li>
</template>

<script>
export default {
  name: 'DiscCard',
  props: {
    imgUrl: String,
    songName: String,
    artist: String,
    year: String,
  },
  // methods: {
  //   addBackground() {

  //   },
  // },
};
</script>

<style lang="scss" scoped>

.content {
  height: 100%;
  background-color: #2E3A46;
  color: gray;
}

h3 {
  color: white;
  line-height: 0.9;
  text-transform: uppercase;
}

</style>
