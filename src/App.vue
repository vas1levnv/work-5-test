<script>
import "bootstrap/dist/css/bootstrap.min.css"
import "bootstrap"
import SideBar from "@/components/sidebar.vue";
import Breadcrumb from "@/components/breadcrumb.vue";
import HeaderPerson from "@/components/header-person.vue";
import MainPage from "@/components/shops-page.vue";
import ShopsPage from "@/components/shops-page.vue";

export default {
  components: {ShopsPage, MainPage, HeaderPerson, Breadcrumb, SideBar},
  data() {
    return {
      isActiveSidebar: false,
    }
  },
  methods: {
    onSidebarActive() {
     !this.isActiveSidebar ? this.isActiveSidebar = true : this.isActiveSidebar = false
    }
  }
}
</script>

<template>
  <div class="app">
    <side-bar :sidebar="isActiveSidebar"></side-bar>
    <div class="header d-lg-flex align-items-center justify-content-between">
      <breadcrumb></breadcrumb>
      <header-person></header-person>
      <div class="btn-sidebar d-lg-none pe-3" @click="onSidebarActive">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-list"
             viewBox="0 0 16 16">
          <path fill-rule="evenodd"
                d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
        </svg>
      </div>
    </div>
    <shops-page></shops-page>
  </div>
</template>

<style>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  min-height: 100vh;
  max-width: 100vw;
  background: #F8FAFF;
  font-size: 0.875rem;
  font-weight: 500;
  display: grid;
  grid-template-columns: auto  1fr;
  grid-template-rows: auto  1fr;
  gap: 59px;
  color: #7D7D7D;
  font-family: "Roboto", sans-serif;
  overflow-x: hidden;
}

.btn-sidebar{
  cursor: pointer;
  width: 30px;
  height: 30px;
}

.btn-sidebar svg{
  width: 100%;
  height: 100%;
}


@media (max-width: 992px) {
  .app {
    grid-template-columns: 1fr;
    padding: 1rem;
    grid-template-rows: auto 1fr;
  }

  .btn-sidebar{
    position: absolute;
    top: 1rem;
    right: 1rem;
  }
}


</style>
