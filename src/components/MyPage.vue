<template>
  <div class="info-title">
    내정보
    </div>
    <hr />

    <div class="wrapper">
      <div class="body-regi">
        <div class="info-card" style="border:1px solid blue">

          <div class="input-id" style="border:1px solid red">
            <label for="Rid">아이디
              <Form style="margin-right:100px"></Form></label>
              <Input class="input-blank" type="text" v-model="value" @input="state.form.Rid = $event.target.value"></Input>
            </div>
            
            <div class="input-id" >
              <label for="Rphone">휴대폰 번호
                <Form style="margin-right:100px"></Form></label>
                <Input type="text" class="input-blank" id="Rphone" v-model="value" @input="state.form.Rphone = $event.target.value"></Input>
                
              </div>

          </div>

          
        </div>
      </div>
  </template>
  
  <script>
  
  export default {
    name: 'MyPage',
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
  @media(min-width:1200px){
      .body-regi{
        font-family: 'Noto Sans KR';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
      width:300px;
      position: absolute;
      left:39vw;
      top:100px;
      padding-bottom:100px;
    } 
  }
  .input-id{
  margin-top: 30px;
  width:calc(80vh - 250px);
}
  
  </style>


  
