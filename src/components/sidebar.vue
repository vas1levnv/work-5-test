<template>
  <div class="sidebar"
       :class="{'sidebar-active': sidebar === true}"
  >
    <a href="/" class="sidebar-logo">
      <img :src="logo" alt="logo">
    </a>
    <div class="sidebar-list mt-5">
      <a href="#" v-for="item in sidebarList" :key="item.id"
         class="sidebar-list-item d-flex align-items-center mb-4 text-decoration-none">
        <div class="sidebar-list-item-img d-flex align-items-center me-3">
          <img :src="item.img" alt="">
        </div>
        <div class="sidebar-list-item-text">
          {{ item.title }}
        </div>
      </a>
    </div>
  </div>
</template>

<script>
import logo from '../assets/img/LogoWork5.png'
import sidebar1 from '../assets/img/sidebar-icon1.svg'
import sidebar2 from '../assets/img/sidebar-icon2.svg'
import sidebar3 from '../assets/img/sidebar-icon3.svg'
import sidebar4 from '../assets/img/sidebar-icon4.svg'
import sidebar5 from '../assets/img/sidebar-icon5.svg'
import sidebar6 from '../assets/img/sidebar-icon6.svg'
import sidebar7 from '../assets/img/sidebar-icon7.svg'
import sidebar8 from '../assets/img/sidebar-icon8.svg'
import sidebar9 from '../assets/img/sidebar-icon9.svg'


export default {
  name: "side-bar",
  props: {sidebar: Boolean},
  data() {
    return {
      logo,
      sidebarList: [
        {id: 1, title: 'Главная', img: sidebar1},
        {id: 2, title: 'Мои магазины', img: sidebar2},
        {id: 3, title: 'Промоматериалы', img: sidebar3},
        {id: 4, title: 'Статистика', img: sidebar4},
        {id: 5, title: 'Баланс', img: sidebar5},
        {id: 6, title: 'Персональные данные', img: sidebar6},
        {id: 7, title: 'FAQ', img: sidebar7},
        {id: 8, title: 'Техподдержка', img: sidebar8},
        {id: 9, title: 'Выход', img: sidebar9},
      ],
    }
  }
}


</script>

<style scoped lang="scss">

.sidebar {
  background: white;
  width: 256px;
  height: 100%;
  padding: 30px 25px;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  position: fixed;
  top: 0;
  z-index: 20;
}

.sidebar-list-item {
  color: #7D7D7D;
  position: relative;

  &:before {
    transition: all 0.3s ease;
    content: '';
    position: absolute;
    top: -10px;
    left: -25px;
    height: 200%;
    width: 4px;
    background: transparent;
  }

  &:hover {
    .sidebar-list-item-img {
      filter: brightness(0) saturate(100%) invert(43%) sepia(89%) saturate(1175%) hue-rotate(216deg) brightness(81%) contrast(96%);
    }

    &:before {
      background: #6666CC;
    }

    .sidebar-list-item-text {
      color: black;
    }
  }

  &-img {
    transition: all 0.3s ease;
    filter: brightness(0) saturate(100%) invert(52%) sepia(6%) saturate(16%) hue-rotate(350deg) brightness(93%) contrast(82%);
  }

  &-text {
    transition: all 0.3s ease;
  }
}


/*
@media (max-width: 992px) {
  .sidebar{
    display: none;
  }
}*/

.sidebar-active {
  display: block !important;
}

@media (max-width: 992px) {

  .sidebar {
    left: 0;
    transform: translateX(-100%);
    transition: all 0.3s ease;
  }

  .sidebar-active {
    transform: translateX(0);
  }
}


</style>