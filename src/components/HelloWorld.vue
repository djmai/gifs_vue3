<template>
  <section class="candidates-profile-bg vh-90">
    <div class="bg-overlay"></div>
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-6">
          <div class="candidates-profile-details text-center">
            <img
              src="https://avatars.githubusercontent.com/u/9259418?v=4"
              class="img-fluid d-block mx-auto rounded-circle img-thumbnail mb-4"
            />
            <h4 class="text-white candidates-profile-name mb-2">
              Gifs/Stickers Search
            </h4>
            <p class="text-white-50 mb-2">
              <i class="mdi mdi-bank mr-2"></i>MTIE Miguel Martínez
            </p>
            <ul class="candidates-profile-icons list-inline mb-3">
              <li class="list-inline-item text-white-50 pr-2 f-16">
                Full Stack Developer
              </li>
            </ul>

            <div class="row">
              <div class="col-lg-12">
                <div class="card job-detail mt-2 p-4">
                  <div class="job-detail-desc">
                    <p class="text-muted f-14 mb-3">
                      Esta aplicación es parte del curso de Vue 3 en Udemy y
                      estamos aprendiendo a integrar Bootstrap, a trabajar con
                      Rutas y muchas cosas más.
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
body {
  margin-top: 20px;
}

.vh-90 {
  height: 90vh !important;
}
.candidates-profile-bg {
  /* padding: 180px 0px 80px 0px; */
  padding: calc(16vh - 0px) 0px 80px 0px;
  background-image: url("https://www.bootdey.com/img/Content/bg1.jpg");
  background-size: cover;
  position: relative;
  background-position: center center;
}

.candidates-profile-details img {
  max-width: 130px;
  background: transparent;
}

.candidates-profile-details .candidates-profile-name {
  font-weight: 300;
}

.candidates-profile-icons .list-inline-item {
  margin: 0 1px !important;
}

.candidates-profile-social-icons li a {
  height: 32px;
  width: 32px;
  color: rgba(255, 255, 255, 0.7);
  text-align: center;
  font-size: 15px;
  display: inline-block;
  line-height: 30px;
  border-radius: 50%;
  border: 1px solid rgba(255, 255, 255, 0.7);
  -webkit-transition: all 0.5s;
  transition: all 0.5s;
}

.candidates-profile-social-icons li a:hover {
  background-color: #ff4f6c;
  color: #ffffff;
  -webkit-transition: all 0.5s;
  transition: all 0.5s;
  border-color: #ff4f6c;
}

.profile-education-icon {
  border: 1px solid #ececec;
  position: absolute;
  width: 90px;
  height: 90px;
  line-height: 90px;
  font-size: 42px;
  border-radius: 50px;
  top: 0;
  left: 0;
  right: 0;
  margin: 0 auto;
  background-color: #ffffff;
  color: #ff4f6c;
  -webkit-transition: all 0.5s;
  transition: all 0.5s;
}

.candidates-profile-education {
  padding: 64px 24px 24px;
}

.candidates-profile-education:hover .profile-education-icon {
  background-color: #ff4f6c;
  border: 1px solid #ff4f6c;
  color: #ffffff;
  -webkit-transition: all 0.5s;
  transition: all 0.5s;
}

.job-details {
  padding: 210px 0px 60px 0px;
  /* background-image: url("../images/job-details-bg.jpg"); */
  background-size: cover;
  position: relative;
  background-position: center center;
}

.job-detail {
  border: 1px solid #ececec;
  border-radius: 6px;
}

.job-details-desc-item p {
  overflow: hidden;
}

.job-detail-icons li {
  margin: 2px !important;
}

.job-detail-icons li a {
  height: 32px;
  width: 32px;
  color: #ff4f6c;
  text-align: center;
  font-size: 15px;
  display: inline-block;
  line-height: 30px;
  border-radius: 50%;
  border: 1px solid #ff4f6c;
  -webkit-transition: all 0.5s;
  transition: all 0.5s;
}

.job-detail-icons li a:hover {
  background-color: #ff4f6c;
  color: #ffffff;
  -webkit-transition: all 0.5s;
  transition: all 0.5s;
}

.job-detail-time li {
  padding: 10px 4px;
  border-top: 1px solid #ececec;
}

.job-detail-time li:first-child {
  border-top: none;
}
.section {
  padding-bottom: 80px;
  padding-top: 80px;
  position: relative;
}
</style>
