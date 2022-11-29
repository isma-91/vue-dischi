<template>
  <div class=" header d-flex align-items-center justify-content-between p-5">
    <div class="logo">
      <img src="@/img/logo-small.svg" alt="">
    </div>
    <SelectPage @change="filterDiscs" />
  </div>
</template>

<script>
import SelectPage from '@/components/SelectPage.vue';

export default {
  name: 'HeaderPage',
  components: {
    SelectPage,
  },
  data() {
    return {
      choice: 'Qualsiasi',
    };
  },
  methods: {
    filterDiscs(newValue) {
      // console.log('preso', newValue);
      this.$emit('change', newValue);
    },
  },
};
</script>

<style lang="scss" scoped>
.header {
  height: 5vh;
  background-color: #2E3A46;
    img {
      width: 50px;
    }
}
</style>
