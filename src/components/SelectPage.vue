<template>
  <div class="selection">
    <label for="select">
      <select
      class="px-5 py-2"
      v-model="choice"
      @change="changeSelect">
        <option value="Qualsiasi">Qualsiasi</option>
        <option value="Pop">Pop</option>
        <option value="Rock">Rock</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
      </select>
    </label>
  </div>
</template>

<script>
export default {
  name: 'SelectPage',
  data() {
    return {
      choice: 'Qualsiasi',
    };
  },
  methods: {
    changeSelect() {
      this.$emit('change', this.choice);
    },
  },
};
</script>

<style lang="scss" scoped>
select {
font-size: 22px;
border: 3px solid salmon;
border-radius: 10px;
}

select:focus {
  outline: none;
}

</style>
