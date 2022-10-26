<template>
  <header id="headerType" :class="fonts">
    <div class="header__inner">
      <div class="header__logo">
        <a href="/">간식박스</a>
      </div>
      <div class="header__menu">
        <ul>
          <li class="active">
            <a href="#slideTyper">에너지 보충</a>
          </li>
          <li>
            <a href="#imageType">영양식</a>
          </li>
          <li>
            <a href="#imgTextType">24시간</a>
          </li>
          <li>
            <a href="#cardType">식사</a>
          </li>
          <li>
            <a href="#bannerType">키친 박스</a>
          </li>
          <li>
            <a href="#textType">간식박스 설치</a>
          </li>
        </ul>
      </div>
      <div class="header__member">
        <a href="/" class="header__member1"> 온라인 주문하기 </a>
        <a href="/" class="header__member2"> 문의하기 </a>
      </div>
      <div class="header__ham">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
  </header>
</template>
<script>
export default {
  props: {
    fonts: String,
  },
};
</script>
<style>
/* headerType */
.header__inner {
  width: 100%;
  height: 70px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 20px;
  box-sizing: border-box;
  border-bottom: 1px solid #ccc;
  position: fixed;
  left: 0;
  top: 0;
  z-index: 10000;
  background: #fff;
}
.header__logo {
  width: 20%;
  font-size: 30px;
  font-weight: 700;
  text-transform: uppercase;
}

.header__menu {
  width: 60%;
  font-size: 20px;
}
.header__menu li {
  display: inline;
}
.header__menu li a {
  padding: 13px 30px;
  margin: 0 5px;
  transition: background-color 0.3s;
}
.header__menu li a.active {
  background: #000;
  color: #fff;
}
.header__menu li a:hover {
  background-color: #f1f1f1;
  border-radius: 5px;
}
.header__member {
  width: 20%;
  text-align: right;
}
.header__member a {
  font-size: 16px;
  border: 1px solid #000;
  padding: 10px 30px;
  border-radius: 50px;
  transition: all 0.3s;
}
.header__member a:hover {
  background-color: #000;
  color: #fff;
}
.header__member1 {
  margin-right: 30px;
  background: #7ccaf5;
}
.header__member2 {
  margin-right: 10px;
  background: #b5ff6b;
}
/*  */
.figure1 {
  width: 30px;
  height: 30px;
  margin-left: 100px;
}
.header__ham {
  position: absolute;
  right: 10px;
  top: 10px;
  z-index: 1000;
  width: 50px;
  height: 50px;
  display: none;
  cursor: pointer;
}
.header__ham span {
  display: block;
  background: #000;
  width: 30px;
  height: 2px;
  border-radius: 3px;
  margin-left: 10px;
  margin-top: 5px;
  transition: 0.25s margin 0.25s, 0.25s transform;
}
.header__ham span:nth-child(1) {
  margin-top: 18px;
}
.header__ham.active span {
  transition: 0.25s margin, 0.25s transform 0.25s;
}
.header__ham.active span:nth-child(1) {
  margin-top: 25px;
  margin-bottom: -7px;
  transform: rotate(45deg);
}
.header__ham.active span:nth-child(2) {
  transform: rotate(45deg);
}
.header__ham.active span:nth-child(3) {
  margin-top: -2px;
  transform: rotate(135deg);
}
/* 미디어 */
@media (max-width: 1300px) {
  .header__menu {
    position: fixed;
    right: -100%;
    top: 69px;
    background: #fff;
    width: 60%;
    height: 100vh;
    padding: 20px;
    text-align: right;
    transition: right 0.4s ease-in;
  }
  .header__menu ul li {
    display: block;
    margin: 20px;
  }
  .header__menu ul li a {
    padding: 10px;
    white-space: nowrap;
  }
  .header__menu.active {
    right: 0;
  }
  .header__member {
    margin-right: 50px;
  }
  .header__ham {
    display: block;
  }
  .header__logo {
    width: 50%;
  }
  .header__member {
    width: 50%;
  }
}
@media (max-width: 600px) {
}
</style>
