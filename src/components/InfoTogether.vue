<template>
      <hr />
  <div class="info-display">
    <div v-for="i in ex" :key="i">
      <div class="info-card">
        <div style="margin-bottom:20px">
          이것은 행사 이름입니다
          <div class="date-button">지금당장</div>
        </div>
        <div class="info-map" style="margin-bottom:20px">
          위치 지도
        </div>
        <div class="info-detail">
          관련 내용입니다
        </div>
        <div class="toget-button">같이가요</div>
      </div>
      <hr />
    </div>
  </div>
  <BottomNav/>
</template>
  

<script>
import BottomNav from "./BottomNav.vue";
export default {
  name: 'InfoTogether',
  data() {
    return {
      ex: [1, 2, 3]
    }
  },
  components: {
    BottomNav: BottomNav,
  }
}
</script>
  
<style>
@import '../css/Info.css';
</style>
  