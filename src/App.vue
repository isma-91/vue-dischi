<template>
<div class="app">
<HeaderPage @change="change"/>
<MainPage :change-result="filterDiscs"/>
</div>
</template>

<script>
import HeaderPage from '@/components/HeaderPage.vue';
import MainPage from '@/components/MainPage.vue';

export default {
  components: {
    HeaderPage,
    MainPage,
  },
  data() {
    return {
      filterDiscs: 'Qualsiasi',
    };
  },
  methods: {
    change(info) {
      this.filterDiscs = info;
      // console.log(this.filterDiscs);
    },
  },
};
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap';

.app {
  height: 100vh;
}

ul {
  list-style-type: none;
}

</style>
