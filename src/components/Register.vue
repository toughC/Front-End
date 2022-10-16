<template>
  <div class="wrapper">
    <div class="body-regi">
        <h1 style="margin-top:0px">회원가입</h1>
        <label class="check-body" v-for="checkboxes in 3" :key="checkboxes">
          <Input class="checkbox-round" type="checkbox" />
          <span>{{checkList[checkboxes-1]}}</span>
        </label>

        <div class="input-id">
          <label>아이디</label>
          <Form style="margin-top:10px">
            <Input class="input-blank"></Input>
            <button class="input-button" @click="validateCheck">중복확인</button>
            <div class="validate-check" v-if="validate == true">사용할 수 있는 아이디 입니다.</div>
            <div class="validate-check" v-if="validate == false">사용할 수 없는 아이디 입니다.</div>
          </Form>
        </div>
        <div class="input-pw">
          <br/>
          <label>비밀번호</label>
          <Form style="margin-top:10px">
            <Input class="input-blank-pw"></Input>
          </Form>
        </div>
        <div class="input-pw">
          <br/>
          <label>비밀번호 확인</label>
          <Form style="margin-top:10px">
            <Input class="input-blank-pw"></Input>
          </Form>
        </div>
        <div class="input-id">
          <label>휴대폰 번호</label>
          <Form style="margin-top:10px">
            <Input class="input-blank"></Input>
            <button class="input-button">인증요청</button>
          </Form>
        </div>
        <div class="input-id">
          <label>인증번호 입력</label>
          <Form>
            <Input class="input-blank"></Input>
            <button class="input-button" style="width:74px">확인</button>
          </Form>
        </div>
        <div class="final-btn">
          <button class="final-button" @click="goSignUp">가입 완료</button>
        </div>
    </div>
  </div>
  </template>
  
  <script>
  
  export default {
    name: 'Register',
    data() {
        return {
          checkList : ['개인정보 수집 및 이용 동의', '위치 정보 수집 동의', '광고성 수신 동의'],
          validate: false
        }
    },
    methods:{
      validateCheck(){
        this.validate = true;
      },
      goSignUp(){
        this.$router.push('/')
      }
    },
    components: {
        
    }
  }
  </script>
  
  <style>
  @media(min-width:1200px){
      .body-regi{
      width:300px;
      position: absolute;
      left:39vw;
      top:100px;
      padding-bottom:100px;
    } 
  }

  @media(min-width:576px) and (max-width:1199px){
      .body-regi{
      width:300px;
      position: absolute;
      left:28vw;
      top:100px;
      padding-bottom:100px;
    } 
  }

  @media (min-width: 768px) and (max-width: 991px) {
    .body-regi{
      width:300px;
      position: absolute;
      left:10vw;
      top:100px;
      padding-bottom:100px;
    } 
  }

  @media(min-width:376px) and (max-width: 575px){
    .body-regi{
      width:300px;
      position: absolute;
      left:10vw;
      top:100px;
      padding-bottom:100px;
    }
  }

  @media(max-width: 375px){
    .body-regi{
      width:300px;
      position: absolute;
      left:13vw;
      top:100px;
      padding-bottom:100px;
    }
  }

  .body-regi h1{
    width:calc(80vh - 250px);
  }

  .check-body{
    display: flex;
    vertical-align: middle;
  }

  .body-regi span{
    vertical-align: middle;
    color:#4B4B4B;
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

.checkbox-round:checked {
    background-color: #E37A39;
}

.input-id{
  margin-top: 30px;
  width:calc(80vh - 250px);
}

.input-blank{
  border: 1px solid #D9D9D9;
  border-radius: 30px;
  padding: 10px;
  padding-right: 34px;
  width:calc(70vh - 310px);
}

.input-button{
  border:0px;
  border-radius: 30px;
  padding:10px;
  margin-left: 1%;
  background: #E37A39;
  color: white;
}

.validate-check{
  color: #E37A39;
  font-size: 12px;
  margin-top: 8px;
}

.input-pw{
  width:calc(50vh - 100px);
}

.input-blank-pw{
  border: 1px solid #D9D9D9;
  border-radius: 30px;
  padding: 10px;
  width:calc(72vh - 250px);
  padding-right: 10%;
}

.final-btn{
  width:calc(75vh - 230px);
}

.final-button{
  border:0px;
  border-radius: 30px;
  background: #2F3F67;
  color:white;
  font-weight: 600;
  font-size:19px;
  margin-top: 30px;
  padding-top:13px;
  padding-bottom:13px;
  width:100%;
}
  </style>
  