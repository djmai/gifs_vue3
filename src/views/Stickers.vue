<template>
  <div id="gifs" class="container mt-3 border">
    <h1 class="text-center">Stickers</h1>
    <search :getSearch="getStickers" />
    <hr />
    <loading v-if="load" />
    <div v-else class="row">
      <div class="col-md-4 col-lg-3" v-for="sticker in stickers" :key="sticker.id">
        <sticker-card :data="sticker" />
      </div>
    </div>
  </div>
</template>

<script>
import Loading from "../components/Loading.vue";
import StickerCard from "../components/StickerCard.vue";
import Search from "../components/Search.vue";

export default {
  components: { StickerCard, Search, Loading },
  data: () => ({
    stickers: {},
    load: true,
  }),
  created() {
    this.getStickers();
  },
  methods: {
    async getStickers(search) {
      this.load = true;
      const api_key = "2T5hcDzeX0vXTc3d4uFuJXGkhRrzDl2P";
      search = search == "" || search == undefined ? "stickers" : search;
      const api = `https://api.giphy.com/v1/stickers/search?q='${search}'&api_key=${api_key}`;
      const { data } = await this.axios.get(api);
      this.stickers = data.data;
      this.load = false;
    },
  },
};
</script>

<style></style>
