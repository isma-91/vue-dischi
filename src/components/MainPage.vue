<template>
  <div class="body d-flex">
    <ul v-if="(arrDiscs && changeResult === 'Qualsiasi')"
    class="row row-cols-5 container m-auto g-4">
      <DiscCard
        v-for="disc in arrDiscs"
        :key="disc.poster"
        :imgUrl= "disc.poster"
        :songName= "disc.title"
        :artist= "disc.author"
        :year= "disc.year"
      />
    </ul>

    <ul v-else-if="arrDiscs" class="row row-cols-5 container m-auto g-4">
      <DiscCard
        v-for="disc in filteredDiscs"
        :key="disc.poster"
        :imgUrl= "disc.poster"
        :songName= "disc.title"
        :artist= "disc.author"
        :year= "disc.year"
      />
    </ul>

    <div class="loading d-flex m-auto" v-else>
      <div>Loading ...</div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'; // Quando nello script senza un percorso prima, parte dalla node modules
import DiscCard from '@/components/DiscCard.vue';

export default {
  name: 'MainPage',
  props: {
    changeResult: String,
  },
  components: {
    DiscCard,
  },
  data() {
    return {
      arrDiscs: null,
      urlApi: 'https://flynn.boolean.careers/exercises/api/array/music',
    };
  },
  created() {
    setTimeout(() => {
      axios.get(this.urlApi)
        .then((axiosResult) => {
        // console.log(axiosResult);
          this.arrDiscs = axiosResult.data.response;
          console.log(axiosResult.data.response);
        });
    }, 1000);
  },
  computed: {
    filteredDiscs() {
      return this.arrDiscs.filter((objDisc) => objDisc.genre === this.changeResult);
    },
  },
};
</script>

<style lang="scss" scoped>
.body {
  background-color: #1E2D3B;
  height: 95vh;
}

.loading {
  font-size: 50px;
  color: white;
  font-weight: bold;
}
</style>
