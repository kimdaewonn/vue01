<template>
  <section id="cardType" class="card__wrap" :class="attr">
    <h2 class="blind">카드 영역</h2>
    <h2>{{ CardType[0].h2 }}</h2>
    <p>{{ CardType[0].p }}</p>
    <div class="card__inner" :class="layout">
      <article class="card" v-for="card in Card" v-bind:key="card.cardInner">
        <figure class="card__header">
          <img :src="card.img" alt="도시락" />
        </figure>
        <div class="card__body">
          <h3 class="tit">{{ card.h3 }}</h3>
          <p class="desc">
            {{ card.p }}
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <!-- <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/card_bg01.jpg" alt="도시락" />
        </figure>
        <div class="card__body">
          <h3 class="tit">도시락</h3>
          <p class="desc">
            고기중심 도시락, 스테이크 도시락, 치킨 도시락, 비빔밥형 도시락,
            새우튀김 도시락, 돈까스 도시락, 야채도시락 등 다양한 도시 락이
            준비되어 있습니다.
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>

      <article class="card">
        <figure>
          <img src="assets/img/card_bg02.jpg" alt="샐러드" />
        </figure>
        <div class="card__body">
          <h3 class="tit">샐러드</h3>
          <p class="desc">
            샐러드 별로 드레싱도 다르고 황금 공식이란것이 존재합니다. 감자
            샐러드, 그린 샐러드, 멕시칸 샐러드, 시저 샐러드 등 다양한 샐러드가
            준비되어 있습니다.
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure>
          <img src="../../assets/img/card_bg03.jpg" alt="샌드위치" />
        </figure>
        <div class="card__body">
          <h3 class="tit">샌드위치</h3>
          <p class="desc">
            잼 샌드위치, 참치 샌드위치, 치즈 샌드위치, 햄치즈 샌드위치, 땅콩버터
            샌드위치, 달걀 샌드위치, 야채 샌드위치, 치킨 샌드위치 등 다양한
            종류가 준비되어 있습니다.
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article> -->
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
      CardType: [
        {
          h2: "도시락 부터 샐러드 까지",
          p: "신선한 품질과 좋은 식사를 합리적인 가격으로 만나볼 기회!!",
        },
      ],
      Card: [
        {
          h3: "도시락",
          p: "고기중심 도시락, 스테이크 도시락, 치킨 도시락, 비빔밥형 도시락,새우튀김 도시락, 돈까스 도시락, 야채도시락 등 다양한 도시락이 준비되어 있습니다.",
          img: "../../assets/img/card_bg01.jpg",
        },
        {
          h3: "샐러드",
          p: "샐러드 별로 드레싱도 다르고 황금 공식이란것이 존재합니다. 감자 샐러드, 그린 샐러드, 멕시칸 샐러드, 시저 샐러드 등 다양한 샐러드가 준비되어 있습니다.",
          img: "../../assets/img/card_bg02.jpg",
        },
        {
          h3: "샌드위치",
          p: "잼 샌드위치, 참치 샌드위치, 치즈 샌드위치, 햄치즈 샌드위치, 땅콩버터 샌드위치, 달걀 샌드위치, 야채 샌드위치, 치킨 샌드위치 등 다양한 종류가 준비되어 있습니다.",
          img: "../../assets/img/card_bg03.jpg",
        },
      ],
    };
  },
};
</script>
<style>
/* cardType */
.card__inner {
  display: flex;
  justify-content: space-between;
}
.card {
  width: 32%;
  background-color: #f5f5f5;
}
.card__body {
  padding: 24px;
}
.card__body .tit {
  font-size: 24px;
  margin-bottom: 10px;
  /* 1줄효과 */
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
.card__body .desc {
  font-size: 18px;
  line-height: 1.4;
  color: #666;
  margin-bottom: 20px;
  font-weight: 300;
  /* 3줄효과 */
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
}
@media (max-width: 960px) {
  .card__inner {
    flex-wrap: wrap;
  }
  .card {
    width: 49%;
  }
  .card:last-child {
    display: none;
  }
}
@media (max-width: 600px) {
  .card {
    width: 100%;
  }
  .card:first-child {
    margin-bottom: 20px;
  }
  .card__body {
    padding: 20px;
  }
  .card__body .desc {
    font-size: 16px;
  }
}
</style>
