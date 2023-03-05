<template>
  <div class="header-person d-flex p-lg-3">
    <div class="header-person-message p-4 me-3">
      <div class="header-person-message-icon">
        <svg width="24" height="18" viewBox="0 0 24 18" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
              d="M21.3295 0H3.10018C2.05806 0 1.21326 0.844805 1.21326 1.88692V16.1127C1.21326 17.1548 2.05806 17.9996 3.10018 17.9996H21.3295C22.3716 17.9996 23.2164 17.1548 23.2164 16.1127V1.88692C23.2164 0.844805 22.3716 0 21.3295 0Z"
              fill="#7B7B7B"/>
          <path d="M1 4.52862L10.7792 11.6989C11.5176 12.2404 12.7317 12.2404 13.4701 11.6989L23.4298 4.39735"
                stroke="white" stroke-width="0.75477" stroke-miterlimit="22.9256"/>
        </svg>
        <div class="header-person-message-icon-dot">
        </div>
      </div>
    </div>
    <div class="header-person-profile d-flex align-items-center">
      <div class="header-person-profile-img me-3">
        <img :src="profile" alt="">
      </div>
      <div class="header-person-profile-name">
        Максим Добжанский
      </div>
    </div>
  </div>
</template>

<script>
import profile from '../assets/img/profile.jpeg'
export default {
  name: "header-person",
  data(){
    return{
      profile
    }
  }
}
</script>

<style scoped lang="scss">
.header-person {
  margin-left: auto;
  &-message {
    border: 1px solid #D4D4D4;
    border-radius: 16px;

    &-icon {
      position: relative;

      &-dot {
        position: absolute;
        top: -3px;
        right: -3px;
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background: white;
        display: flex;
        justify-content: center;
        align-items: center;

        &:before {
          content: '';
          width: 7px;
          height: 7px;
          border-radius: 50%;
          background: red;
        }
      }
    }

  }

  &-profile{
    padding: 10px 17px;
    box-shadow: 0px 0px 16px rgba(136, 167, 245, 0.18);
    border-radius: 16px;
    &-img{
      width: 50px;
      height: 50px;
      border: 2px solid #D9D9D9;
      border-radius: 50%;
      overflow: hidden;
      & img{
        width: 100%;
        object-fit: cover;
      }
    }
  }
}
</style>