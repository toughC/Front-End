<template>
  <div class="info-title">
    해운대구
    <div class="info-map-icon"></div>
    <hr />
  </div>
  <div style="margin-bottom:20px">
    <label class="switch-button">
      <input type="checkbox" />
      <span class="onoff-switch"></span>
    </label>
    <span class="switch-text">정보공유</span>
  </div>
<div v-for="i in ex" :key="i">

  <div style="margin-bottom:20px">
    이것은 행사 이름입니다 
    <div class="date-button">지금당장</div>
  </div>
  <div class="info-map" style="margin-bottom:20px">
    위치 지도
  </div>
  <div>
    관련 내용입니다
  </div>
  <hr />
</div>
</template>
  
<script>
export default {
  name: 'InfoShare',
  data() {
    return {
      ex : [ 1,2,3]
    }
  },
  components: {

  }
}
</script>
  
<style>
@import '../css/Info.css';
</style>
  
  