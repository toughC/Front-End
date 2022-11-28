<template>
  <div>
    <div class="info-title">
    내정보
  </div>
  <hr />
  <div class="body-regi">
        <div class="container">
          <br />
          <label for="Myid">아이디
            <Form style="margin-right:150px"></Form>
          </label>
          <Input class="my-input-blank" type="text" disabled="true" v-model="value" @input="state.form.Rid = $event.target.value"></Input>
        </div>

        <div class="container">
          <br />
          <label for="Myphone">휴대폰 번호
            <Form style="margin-right:150px"></Form>
          </label>
          <Input type="text" class="input-blank" id="Rphone" v-model="value"
            @input="state.form.Rphone = $event.target.value"></Input>
        </div>
      
        <div class="container">
          <br />
          <label for="Mypw">비밀번호
            <Form style="margin-right:150px"></Form>
          </label>
          <Input type="text" class="input-blank" v-model="value"
            @input="state.form.Rpw = $event.target.value, console.log(state.form.Rpw)"></Input>
          </div>

          <div class="container">
          <br />
          <label for="MypwCheck" >비밀번호 확인
            <Form style="margin-right:150px"></Form>
          </label>
          <Input class="input-blank" type="text" v-model="value" @input="state.form.Rid = $event.target.value"></Input>
            </div>
        </div>
        
      </div>
</template>



<script>
import { reactive } from '@vue/reactivity'

export default {
  name: 'MyPage',
  setup(){
    const state = reactive({ 
      loggedIn:false,
        account:{
          mid: null,
          memberName: "",
        },
        form:{
          Myid: "",
          Mypw: "",
          MypwCheck: "",
          Myphone: "",
        },
    });
    return {state}
  },
  data() {
    return {

    }
  },
  components: {

  }
}
</script>
  
<style>
@import url(https://fonts.googleapis.com/earlyaccess/notosanskr.css);

@media(min-width:1200px) {
  .body-regi {
    font-family: 'Noto Sans KR';
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    width: 300px;
    position: absolute;
    left: 39vw;
    top: 100px;
    padding-bottom: 100px;
  }
}

@media(min-width:576px) and (max-width:1199px) {
  .body-regi {
    font-family: 'Noto Sans KR';
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    width: 300px;
    position: absolute;
    left: 28vw;
    top: 100px;
    padding-bottom: 100px;
  }
}

@media (min-width: 768px) and (max-width: 991px) {
  .body-regi {
    font-family: 'Noto Sans KR';
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    width: 300px;
    position: absolute;
    left: 10vw;
    top: 100px;
    padding-bottom: 100px;
  }
}

@media(min-width:377px) and (max-width: 575px) {
  .body-regi {
    font-family: 'Noto Sans KR';
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    width: 300px;
    position: absolute;
    left: 10vw;
    top: 100px;
    padding-bottom: 100px;
  }
}

@media(max-width: 376px) {
  .body-regi {
    width: 300px;
    position: absolute;
    left: 14vw;
    top: 100px;
    padding-bottom: 100px;
  }
}

.container {
  display:flex;
  align-items: center;
  height: 100px;
}

.body-regi h1 {
  width: calc(80vh - 250px);
}

.check-body {
  display: flex;
  vertical-align: middle;
}

.body-regi span {
  vertical-align: middle;
  color: white;
  overflow: visible;
}

.checkbox-round {
  width: 1.3em;
  height: 1.3em;
  background-color: white;
  border-radius: 50%;
  vertical-align: middle;
  border: 1px solid #ddd;
  appearance: none;
  -webkit-appearance: none;
  outline: none;
  cursor: pointer;
}

.modal-button {
  border: 0px;
  background: white;
}

.checkbox-round:checked {
  background-color: #E37A39;
}

.my-input-id {
  margin-right: 100px;
  width: calc(80vh - 250px);
}

.my-input-blank {
  background: lightgray;
  border: 1px solid #D9D9D9;
  border-radius: 30px;
  padding: 10px;
  padding-right: 34px;
  width: calc(70vh - 310px);
}

.my-input-pw {
  margin-right: 80px;
  width: calc(80vh - 50px);
}

.my-input-blank-pw {
  border: 1px solid #D9D9D9;
  border-radius: 30px;
  padding: 10px;
  width: calc(72vh - 250px);
  padding-right: 10%;
}

.final-btn {
  width: calc(75vh - 230px);
}

.final-button {
  border: 0px;
  border-radius: 30px;
  background: #2F3F67;
  color: white;
  font-weight: 600;
  font-size: 19px;
  margin-top: 30px;
  padding-top: 13px;
  padding-bottom: 13px;
  width: 100%;
}

.modal-scroll {
  overflow-y: auto;
}
</style>
  
