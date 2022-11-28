<template>
<div class="app">
<HeaderPage />
<MainPage />
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
};
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap';

.app {
  height: 100vh;
}

</style>
