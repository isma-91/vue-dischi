<template>
  <div class="body">
    <DiscCard />
  </div>
</template>

<script>
import axios from 'axios'; // Quando `nello script senza un percorso prima, parte dalla node modules
import DiscCard from '@/components/DiscCard.vue';

export default {
  name: 'MainPage',
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
    axios.get();
  },
};
</script>

<style lang="scss" scoped>
.body {
  background-color: #1E2D3B;
  height: 95vh;
}
</style>
