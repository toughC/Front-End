<template>
  <div class="post-title">
    정보작성
    <hr />
  </div>
  <div class="post-display">
    <div>
      행사제목
      <Input class="post-input"></Input>
    </div>
    <div>
      <div class="post-label">
        위치
      </div>
      <div>
        <Input class="map-input"></Input>
        <div class="post-map-icon">
          <img :src="require('@/img/now_position_icon.svg')" style="width: 38px; height: 38px; padding-top: 5px;" />
        </div>
      </div>
    </div>

    <div class="post-btn-group">
      <div class="date-select-button">지금당장</div>
      <div class="date-select-button">어제 갔다왔음</div>
      <div class="date-select-button">오늘 하더라</div>
      <div class="date-select-button">내일도 한대</div>
    </div>

    <div style="margin-top: 10%;">
      <label class="post-label">내용</label>
      <Input class="post-input-box"></Input>
    </div>
    <div class="final-btn" style="margin:auto">
      <button class="final-button" @click="goSignUp">작성 완료</button>
    </div>
  </div>
</template>
  
<script>

export default {
  name: 'InfoPost',
  data() {
    return {

    }
  },
  components: {

  }
}
</script>
  
<style>
@import '../css/Info.css';
</style>
  