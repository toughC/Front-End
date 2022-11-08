<template>
    <!-- 찜 기능 -->
    <div class="map-detail-heart-container">
      <img :src="require('@/img/heart_false.svg')" style="width: 36px; margin: 15px;" />
    </div>
    

    <!-- 행사 포스터 -->
    <div class="map-detail-poster">
        
    </div>

    <!-- 행사 제목 -->
    <div class="map-detail-event-title">
      {{$route.params.id}}번째 행사
    </div>

    <!-- 정보 container -->
    <div class="map-detail-info-container">
      <ul>
        <!-- 기간 -->
        <li>
          기간
          <div class="map-detail-info-content-of-content">
            2022 . 10 . 9 ~ 2022 . 11 . 9 
          </div>
        </li>

        <!-- 관람 회차 -->
        <li>
          관람 회차
          <div class="map-detail-info-content-of-content">
            11:00 , 12:00 , 17:00 , 18:00  
          </div>
        </li>

        <!-- 가격 -->
        <li>
          가격
          <div class="map-detail-info-content-of-content">
            A석 20000원, R석 40000원  
          </div>
        </li>
      </ul>
    </div>

  </template>
  
  <script>
  
  export default {
    name: 'Detail',
    data() {
        return {

        }
    },
    components: {
        
    }
  }
  </script>
  
  <style>
  @import "../css/detail.css";
  </style>
  