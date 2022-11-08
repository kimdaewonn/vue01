<template>
  <section id="bannerType" class="banner__wrap" :class="fonts">
    <h2 class="blind">배너 영역</h2>
    <div class="banner__inner">
      <h3 class="title">{{ BannerType[0].h3 }}</h3>
      <p class="desc">
        {{ BannerType[0].p }}
      </p>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
  data: function () {
    return {
      BannerType: [
        {
          h3: "키친 박스",
          p: "간편식세트부터 샐러드까지 인원이 적어도 조리시설이 없어도 식사 제공이 가능합니다.",
        },
      ],
    };
  },
};
</script>
<style>
.banner__inner {
  background-image: url(../../assets/img/banner_bg01.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  text-align: center;
  padding: 120px 0;
  color: #fff;
}
.banner__inner .title {
  font-size: 50px;
  line-height: 1;
  font-weight: 600;
  margin-bottom: 40px;
}
.banner__inner .desc {
  font-size: 24px;
  line-height: 1.5;
  font-weight: 550;
  margin-bottom: 70px;
}
.banner__inner .desc a {
  color: #fff;
  display: block;
}
.banner__inner .desc a:hover {
  text-decoration: underline;
}
.banner__inner .small {
  font-size: 16px;
  text-decoration: underline;
}
@media (max-width: 960px) {
  .banner__inner {
    padding: 100px 0;
  }
}
@media (max-width: 600px) {
  .banner__inner {
    padding: 80px 0;
  }
  .banner__inner .title {
    font-size: 30px;
    margin-bottom: 20px;
  }
  .banner__inner .desc {
    font-size: 16px;
    margin-bottom: 40px;
  }
}
</style>
