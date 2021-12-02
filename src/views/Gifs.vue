<template>
  <div id="gifs" class="container mt-3 border">
    <h1 class="text-center">Gifs</h1>
    <search :getSearch="getGifs" />
    <hr />
    <loading v-if="load" />
    <div v-else class="row">
      <div class="col-md-4 col-lg-3" v-for="gif in gifs" :key="gif.id">
        <gif-card :data="gif" />
      </div>
    </div>
  </div>
</template>

<script>
import Loading from "../components/Loading.vue";
import GifCard from "../components/GifCard.vue";
import Search from "../components/Search.vue";

export default {
  components: { GifCard, Search, Loading },
  data: () => ({
    gifs: {},
    load: true,
  }),
  created() {
    this.getGifs();
  },
  methods: {
    async getGifs(search) {
      this.load = true;
      const api_key = "2T5hcDzeX0vXTc3d4uFuJXGkhRrzDl2P";
      search = search == "" || search == undefined ? "gifs" : search;
      const api = `https://api.giphy.com/v1/gifs/search?q='${search}'&api_key=${api_key}`;
      const { data } = await this.axios.get(api);
      this.gifs = data.data;
      this.load = false;
    },
  },
};
</script>

<style></style>
