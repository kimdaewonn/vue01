<template>
  <section id="imgTextType" class="imgText__wrap" :class="attr">
    <h2 class="blind">이미지/텍스트 영역</h2>
    <div class="imgText__inner" :class="layout">
      <div class="imgText__txt">
        <h3>24시간 언제 어디서나 신선하게</h3>
        <p>
          ‘콜드체인 배달 시스템’에 따라<br />
          신선도를 유지해 안전하게 배송되며,<br />
          온도 모니터링 기능이 가능한<br />
          스마트 디바이스로 현장관리자 없이<br />
          24시간 운영 가능한 비대면 플랫폼<br />
          입니다.
        </p>
      </div>
      <div class="imgText__img img1">
        <a href="/">결제 박스</a>
      </div>
      <div class="imgText__img img2">
        <a class="blue" href="/">스낵 박스</a>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
};
</script>
<style>
/* imgTextType */
.imgText__inner {
  display: flex;
  justify-content: space-between;
}
.imgText__inner > div {
  width: 32%;
  height: 500px;
}
/* .imgText__txt {
} */
.imgText__txt span {
  font-size: 16px;
  color: #666;
  text-decoration: underline;
  text-underline-position: under;
  margin-bottom: 20px;
}
.imgText__txt h3 {
  font-size: 47px;
  font-weight: 400;
  word-break: keep-all;
  line-height: 1.4;
  margin-bottom: 20px;
  margin-top: 20px;
}
.imgText__txt p {
  font-size: 24px;
  font-weight: 300;
  line-height: 1.7;
  color: #666;
  margin-bottom: 10px;
}
.imgText__txt ul {
  font-size: 18px;
  width: 300px;
  line-height: 1.6;
}
.imgText__txt ul li {
  position: relative;
  padding-left: 20px;
}
.imgText__txt ul li a {
  color: #666;
}
.imgText__txt ul li::before {
  content: "";
  width: 5px;
  height: 5px;
  border-radius: 50%;
  position: absolute;
  left: 5px;
  top: 9px;
  background: #666;
}
.imgText__img {
  border-radius: 10px;
  position: relative;
}
.imgText__img a {
  position: absolute;
  left: 30px;
  bottom: 30px;
  background-color: #7c2b39;
  color: #fff;
  font-size: 18px;
  padding: 10px 30px;
  border-radius: 30px;
  display: inline-block;
}
.imgText__img a.blue {
  background: #2b387c;
}
.imgText__img.img1 {
  background: url(../../assets/img/imgText_bg01.jpg) no-repeat center / cover;
}
.imgText__img.img2 {
  background: url(../../assets/img/imgText_bg02.jpg) no-repeat center / cover;
}

@media (max-width: 960px) {
  .imgText__inner {
    flex-wrap: wrap;
  }
  .imgText__txt h3 {
    font-size: 40px;
  }
  .imgText__txt p {
    margin-bottom: 60px;
  }
  .imgText__inner > div.imgText__text {
    width: 100%;
    height: auto;
    text-align: center;
  }
  .imgText__inner > div.imgText__text ul {
    display: none;
  }
  .imgText__inner > div.imgText__img {
    width: 50%;
  }
}
@media (max-width: 600px) {
  .imgText__txt span {
    font-size: 14px;
    margin-bottom: 10px;
  }

  .imgText__txt h3 {
    font-size: 30px;
  }
  .imgText__txt p {
    margin-bottom: 50px;
    font-size: 16px;
  }
  .imgText__inner > div.imgText__img {
    width: 100%;
    height: 200px;
  }
  .imgText__inner > div.imgText__img {
    margin-bottom: 20px;
  }
  .imgText__img a {
    left: 20px;
    bottom: 20px;
  }
}
</style>
