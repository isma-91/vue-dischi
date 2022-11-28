<template>
  <div class="col">
    <div class="content">
      <img :src="imgUrl" :alt="songName">
      <h2 class="song-name">{{ songName }}</h2>
      <div class="artist">{{ artist }}</div>
      <div class="year">{{ year }}</div>
    </div>
  </div>
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
};
</script>

<style lang="scss" scoped>
img {
  width: 100%;
}

</style>
