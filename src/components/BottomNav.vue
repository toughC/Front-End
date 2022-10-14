<template>
    <div class="bottom-nav-container-of-container">
        <div class="bottom-nav-container">
            <div class="bottom-nav-item">
                <img :src="require('@/img/infopage_icon_false.svg')" style="width: 40px;"  />
            </div>

            <div class="bottom-nav-item">
                <img :src="require('@/img/map_icon_true.svg')" style="width: 36px;" />
            </div>

            <div class="bottom-nav-item">
                <img :src="require('@/img/mypage_icon_false.svg')" style="width: 40px;" />
            </div>
        </div>
    </div>
  </template>
  
  <script>
  
  export default {
    name: 'BottomNav',
    data() {
        return {

        }
    },
    components: {
        
    }
  }
  </script>
  
  <style>
@import "../css/bottomNav.css";
  </style>
  