<template>
  <div class="card mb-4 box-shadow">
    <img
      loader="lazy"
      class="card-img-top"
      :src="data.images.downsized.url"
      data-holder-rendered="true"
    />
    <div class="card-header">
      {{ data.title == null || data.title == "" ? "Sin Titulo" : data.title }}
    </div>
    <div class="card-body">
      <div class="d-flex justify-content-between">
        <div class="d-flex flex-row align-items-center">
          <a
            :href="data.user ? data.user.profile_url : '#'"
            target="_blank"
            rel="noopener noreferrer"
          >
            <img
              class="avatar avatar-48 bg-light rounded-circle text-white p-2"
              :src="
                data.user
                  ? data.user.avatar_url
                  : 'https://picsum.photos/100/100/'
              "
            />
          </a>
          <div class="ms-2 c-details">
            <h6 class="mb-0">
              {{ data.user ? data.user.display_name : "Anónimo" }}
            </h6>
            <a
              :href="data.user ? data.user.profile_url : '#'"
              target="_blank"
              rel="noopener noreferrer"
            >
              <span>{{ data.user ? data.user.username : "Anónimo" }}</span>
            </a>
          </div>
        </div>
        <div class="badge"><span>Design</span></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    data: Object,
  },
};
</script>

<style scoped></style>
