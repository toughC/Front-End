<template>
  <div class="body-sign">
    <div class="main-title">
        <h1>부산시 문화예술 지도</h1>
    </div>
    <div>
      <div>
        <form class="login-item">
          <FormItem>
            <Input class="login" type="text" v-model="value" placeholder="아이디" @input="id = $event.target.value">
            </Input>
          </FormItem>
          <FormItem>
            <Input class="login" type="text" v-model="value" placeholder="비밀번호" @input="pw = $event.target.value">
            </Input>
          </FormItem>
          <button class="login-button" @click="goMap" v-if="state.loggedIn === true">
            로그인
          </button>
          <button class="login-button" @click="goMap" v-if="state.loggedIn === false" disabled="true">
            로그인
          </button>
        </form>
      </div>
      <br />
      <div class="find-pw" style="color: rgb(243, 115, 33); font-size:13px" v-if="state.loggedIn === false">유효하지 않은 아이디 입니다.</div>
      <div class="regi">
        계정이 없으신가요?
        <div class="register"  @click="goRegister">회원가입</div>
      </div>
      <div class="find-pw">
        비밀번호 찾기
      </div>
    </div>
  </div>
</template>
  
  <script>
  import {reactive} from "vue";

  export default {
    setup(){
      const state = reactive({
        loggedIn:false
      });

      return { state };
    },
    name: 'SignUp',
    data() {
        return {
          id:'',
          pw:'',
          check: '',
        }
    },
    methods:{
      goRegister(){
        this.$router.push("/register");
      },
      goMap(){
        if(this.id == 'admin' && this.pw == '1234'){
          this.$router.push("/Map");
          this.check = true;
        }else{
          this.check = false;
          alert('유효하지 않은 아이디 입니다.')
        }
      }
    },
    components: {
}
  }
  </script>
  
  <style>

  .body-sign{
    place-items:center;
    display:grid;
    min-height: 100vh;
    font-weight: 400;
    font-size: 15px;
  }

  .main-title{
    padding-top:15%;
  }

  .login-item{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .login{
    border: 1px solid #D9D9D9;
    border-radius: 30px;
    padding: 20px;
    margin-top:20px;
    width:280px
  }

  .login-button{
    border: 0px solid #D9D9D9;
    border-radius: 30px;
    margin-top:20px;
    padding: 20px;
    background: rgb(243, 115, 33);
    width:50%;
    height: 46px;
    color:white;
    line-height: 0;
  }

  .regi{
    display: flex;
    flex-direction: row;
    justify-content: center;
  }

  .find-pw{
    display: flex;
    flex-direction: row;
    justify-content: center;
    color: rgb(43, 63, 107);
    font-weight: 600;
    line-height: 40px;
  }

  .register{
    color:rgb(243, 115, 33);
    font-weight: 600;
    margin-left: 10px;
    text-decoration-line: underline;
  }
  </style>
  