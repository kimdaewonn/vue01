<template>
  <section id="imageType" class="image__wrap" :class="attr">
    <h2 class="blind">이미지 영역</h2>
    <h2>간식박스의 특별함</h2>
    <p>신선도, 영양, 균형, 가공단계까지 고려한 간식 = 식품입니다.</p>
    <div class="image__inner" :class="layout">
      <article class="image img1">
        <h3 class="image__title">요거트</h3>
        <p class="image__desc">
          플레인, 딸기, 복숭아, 포도, 파인애플, 고구마, 단호박 등 다양한 맛이
          있습니 다. 또, 소화기 질병, 콜레스테롤 수치 안정에 도움을 주며, 장수
          건강식입니다.
        </p>
        <a class="image__btn" href="/" title="자세히 보기">자세히 보기</a>
      </article>
      <article class="image img2">
        <h3 class="image__title2">과일음료, 과일</h3>
        <p class="image__desc2">
          오렌지 주스, 포도 주스, 토마토 주스, 등 다양하게 준비되어 있습니다.
          과일도 바나나 외에도 사과, 딸기, 귤 등 다양하게 준비되어 있습니다.
        </p>
        <a class="image__btn yellow" href="/" title="자세히 보기"
          >자세히 보기</a
        >
      </article>
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
/* imageType */
.image__inner {
  display: flex;
  justify-content: space-between;
}
.image {
  width: 49%;
  height: 370px;
  color: #fff;
  padding: 200px 30px 30px 30px;
  box-sizing: border-box;
}
.image.img1 {
  background: url(../../assets/img/image_bg01_01.jpg) no-repeat center;
}
.image.img2 {
  background: url(../../assets/img/image_bg01_02.jpg) no-repeat center;
}
.image__title {
  font-size: 32px;
  margin-bottom: 10px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.image__desc {
  font-size: 16px;
  font-weight: 300;
  margin-bottom: 10px;
  line-height: 1.5;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}
.image__btn {
  font-size: 16px;
  color: #fff;
  background-color: #b45a30;
  padding: 10px 20px;
  display: inline-block;
}
.image__btn.yellow {
  background-color: #b59140;
}
.image__title2 {
  font-size: 32px;
  margin-bottom: 10px;
  color: #000;
  font-weight: 400;
}
.image__desc2 {
  font-size: 16px;
  font-weight: 400;
  margin-bottom: 10px;
  line-height: 1.5;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  color: #000;
}
@media (max-width: 960px) {
}
@media (max-width: 600px) {
  .image__inner {
    flex-direction: column;
  }
  .image {
    width: 100%;
    padding: 205px 20px 20px 20px;
  }
  .image:first-child {
    margin-bottom: 20px;
  }
  .image__title {
    font-size: 24px;
  }
  .image__desc {
    font-size: 16px;
  }
}
</style>
