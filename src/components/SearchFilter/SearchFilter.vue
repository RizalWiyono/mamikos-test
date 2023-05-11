<!-- eslint-disable prettier/prettier -->
<template>
  <input 
    ref="inputSearch" 
    v-model="searchTerm" 
    type="search" 
    @input="handleSearchInputChange" 
    :placeholder="placeholder"
  />
</template>
<!-- eslint-disable prettier/prettier -->

<script>
export default {
  name: "SearchFilter",
  props: {
    placeholder: {
      type: String,
      required: true,
    },
    searchAction: {
      type: Function,
      required: true,
    },
  },
  data() {
      return {
        searchTerm: "",
      }
  },
  methods: {
    handleSearchInputChange() {
      this.searchAction(this.searchTerm)
		},
  }
};
</script>
<!-- eslint-disable prettier/prettier -->

<style scoped>
  input {
    padding: 10px;
    width: 300px;
    border: 0;
    border-radius: 8px;
    cursor: pointer;
    border: 1px solid #d3d3d3;
  }
</style>
