<template>
  <!-- <form @submit.prevent="ejecutarPeticion"> -->
  <form @submit.prevent="getSearch(search)">
    <div class="input-group mb-3">
      <span class="input-group-text">Buscador</span>
      <input
        v-model="search"
        type="text"
        class="form-control"
        placeholder="Examples: burrito apple heart house casa"
      />
      <button class="btn btn-secondary" type="submit">
        <i class="bi bi-search"></i>
      </button>
    </div>
  </form>
</template>

<script>
export default {
  data: () => ({
    search: "",
  }),
  props: {
    getSearch: Function,
  },
  // methods: {
  //   ejecutarPeticion() {
  //     this.$emit("accion", this.search);
  //   },
  // },
};
</script>

<style></style>
