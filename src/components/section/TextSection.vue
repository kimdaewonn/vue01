<template>
  <section id="textType" class="text__wrap" :class="attr">
    <h2 class="blind">텍스트 영역</h2>

    <span>{{ TextType[0].small }}</span>
    <h2 class="mb70">{{ TextType[0].h2 }}</h2>
    <div class="text__inner" :class="layout">
      <div
        class="text"
        :class="text.img"
        v-for="text in Text"
        v-bind:key="text.TextInner"
      >
        <h3 class="text__title">{{ text.h3 }}</h3>
        <p class="text__dsec">
          {{ text.p }}
        </p>
        <a class="text_btn" href="/">{{ text.btn }}</a>
      </div>
      <!-- <div class="text t2">
        <h3 class="text__title">2. 고객사 방문</h3>
        <p class="text__dsec">
          전문 컨설턴트가 직접 방문하여 주변 식당/매점 유무 등을 확인하고
          유동인원, 환경에 맞춰 간식박스 설치 최적 장소를 추천해드립니다.
        </p>
        <a class="text_btn" href="/">더보기</a>
      </div>
      <div class="text t3">
        <h3 class="text__title">3. 조건협의, 계약</h3>
        <p class="text__dsec">
          고객사 맞춤 상품 제안과 선택, 복지 지원금 에 따른 상품 가격, 월 예상
          금액 등 비용,운 영 조건 협의후 계약이 진행됩니다.
        </p>
        <a class="text_btn" href="/">더보기</a>
      </div>
      <div class="text t4">
        <h3 class="text__title">4. 설치 및 운영</h3>
        <p class="text__dsec">
          간식박스는 설치와 동시에 바로 운영이 가능 합니다.전문 배송기사님이
          주기적으로 방문, 관 리해드리며 데이터 기반 진열 종류,수량을 조정
        </p>
        <a class="text_btn" href="/">더보기</a>
      </div>
      <div class="text t5">
        <h3 class="text__title">5. 월 마감</h3>
        <p class="text__dsec">
          기존 간식 업무에서 복잡하고 골치 아팠던 회 계처리. 수많은 영수증,
          바뀌는 업체관리 이 모 든게 한 장의 거래 명세서로 해결됩니다.
        </p>
        <a class="text_btn" href="/">더보기</a>
      </div>
      <div class="text t6">
        <h3 class="text__title">6. 피드백</h3>
        <p class="text__dsec">
          간식 박스는 마감 이후 불편했던 점, 개선 했으면 좋겠는 점 등을
          적극적으로 수용하 여 개선하기위해 노력합니다.
        </p>
        <a class="text_btn" href="/">더보기</a>
      </div> -->
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
      TextType: [
        {
          h2: "간식 박스 설치",
          small: "과정을 알아봅시다.",
        },
      ],
      Text: [
        {
          h3: "1. 상담접수",
          p: "홈페이지를 통해 상담 문의를 남겨주시면 고객 사의 규모, 업종, 성비, 비용에 맞춰 적합한 기기 와 서비스 타입을 제안하는 1차 상담을 진행.",
          btn: "더보기",
          img: "t1",
        },
        {
          h3: "2. 고객사 방문",
          p: "전문 컨설턴트가 직접 방문하여 주변 식당/매점 유무 등을 확인하고 유동인원, 환경에 맞춰 간식박스 설치 최적 장소를 추천해드립니다.",
          btn: "더보기",
          img: "t2",
        },
        {
          h3: "3. 조건협의, 계약",
          p: "고객사 맞춤 상품 제안과 선택, 복지 지원금 에 따른 상품 가격, 월 예상금액 등 비용,운 영 조건 협의후 계약이 진행됩니다.",
          btn: "더보기",
          img: "t3",
        },
        {
          h3: "4. 설치 및 운영",
          p: "간식박스는 설치와 동시에 바로 운영이 가능 합니다.전문 배송기사님이 주기적으로 방문, 관 리해드리며 데이터 기반 진열 종류,수량을 조정",
          btn: "더보기",
          img: "t4",
        },
        {
          h3: "5. 월 마감",
          p: "기존 간식 업무에서 복잡하고 골치 아팠던 회 계처리. 수많은 영수증, 바뀌는 업체관리 이 모 든게 한 장의 거래 명세서로 해결됩니다.",
          btn: "더보기",
          img: "t5",
        },
        {
          h3: "6. 피드백",
          p: "간식 박스는 마감 이후 불편했던 점, 개선 했으면 좋겠는 점 등을 적극적으로 수용하 여 개선하기위해 노력합니다.",
          btn: "더보기",
          img: "t6",
        },
      ],
    };
  },
};
</script>
<style>
/* textType */
.text__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.text {
  width: 32%;
  margin-bottom: 2%;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 10px;
  transition: background 0.4s;
}
.text:hover {
  background: #f5f5f5;
}
.text__title {
  font-size: 24px;
  line-height: 1;
  margin-bottom: 10px;
  white-space: nowrap;
  text-overflow: ellipsis;
  position: relative;
  padding-top: 75px;
  font-weight: 400;
}
.text__title::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 60px;
  height: 60px;
  background: url(../../assets/img/text_icon.svg);
}
.text.t1 .text__title::before {
  background-position: 0 0;
}
.text.t2 .text__title::before {
  background-position: -60px 0;
}
.text.t3 .text__title::before {
  background-position: -120px 0;
}
.text.t4 .text__title::before {
  background-position: -180px 0;
}
.text.t5 .text__title::before {
  background-position: -240px 0;
}
.text.t6 .text__title::before {
  background-position: -300px 0;
}
.text__dsec {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.4;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  color: #666;
  margin-bottom: 20px;
}
.text_btn {
  font-size: 16px;
  line-height: 1;
  text-decoration: underline;
  text-underline-position: under;
  color: #666;
}
.section > span {
  display: block;
  text-align: center;
  font-size: 16px;
  text-decoration: underline;
  margin-bottom: 20px;
}

@media (max-width: 960px) {
  .text {
    width: 48%;
    background: #f5f5f5;
  }
}
@media (max-width: 600px) {
  .text__title {
    font-size: 20px;
  }
  .text__desc {
    font-size: 16px;
  }
}
@media (max-width: 480px) {
  .text {
    width: 100%;
  }
}
</style>
