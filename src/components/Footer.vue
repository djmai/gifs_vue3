<template>
  <footer
    class="d-flex flex-wrap justify-content-between align-items-center border-top bg-dark bg-gradient text-white"
  >
    <div class="col-md-4 d-flex align-items-center my-3 mx-3">
      <span>© {{ year }} - {{ autor }}</span>
    </div>

    <ul
      class="nav col-md-4 justify-content-end list-unstyled d-flex text-white my-3 mx-3"
    >
      <li class="ms-3">
        <a class="text-white" href="https://twitter.com/DjMai">
          <i class="bi bi-twitter"></i>
        </a>
      </li>
      <li class="ms-3">
        <a class="text-white" href="https://www.instagram.com/mrmiguelillo/">
          <i class="bi bi-instagram"></i>
        </a>
      </li>
      <li class="ms-3">
        <a class="text-white" href="https://www.facebook.com/mmmv88">
          <i class="bi bi-facebook"></i>
        </a>
      </li>
    </ul>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data: () => ({
    //   autor: ''
  }),
  props: {
    autor: {
      type: String,
      default: "MTIE Miguel Martínez",
    },
  },
  computed: {
    year() {
      return new Date().getFullYear();
    },
  },
};
</script>

<style>
Footer {
  position: fixed;
  bottom: 0;
  width: 100%;
}
</style>
