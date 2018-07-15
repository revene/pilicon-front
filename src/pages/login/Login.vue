<template>
  <div class="background">
    <header class="header">
      <div class="header-left">
        <i class="iconfont">&#xe612;</i>
        pilicon
      </div>
      <div class="header-center"></div>
      <div class="header-right">write by bl</div>
    </header>
    <section class="body">
      <div class="middle">
        <div class="middle-show">
          <span id="title">欢迎来到pilicon.com</span>
        </div>
        <div class="middle-regist">
          <table class="regist">
            <thead class="thead">
              <tr class="tr">
                <td  class="td"  @click="switchLogin">猪猡注册</td>
                <td  class="td"  @click="switchLogin">猪猡登录</td>
              </tr>
            </thead>
          </table>
          <div v-if="loginFlag==true">
            <input class="input inputName" name="usercode" type="text" v-model="user.userName" placeholder="请输入猪猡号">
            <input class="input inputPwd" name="password" type="password" v-model="user.password" placeholder="请输入猪猡密码">
            <button class="button" type="submit" @click="login">登录</button>
            <span class="forget">忘记密码?猡,我也没办法</span>
          </div>
          <div v-if="loginFlag==false">
            <input class="input inputName" name="usercode" type="text" v-model="user.userName" placeholder="请输入猪猡号">
            <input class="input inputPwd" name="password" type="password" v-model="user.password" placeholder="请输入猪猡密码">
            <input class="input inputRePwd" name="password" type="password" v-model="user.rePassword" placeholder="请重复猪猡密码">
            <button class="button" type="submit" @click="regist">注册</button>
            <span class="forget">忘记密码?猡,我也没办法</span>
          </div>
        </div>
      </div>
    </section>
    <footer class="footer">

    </footer>
  </div>
</template>

<script>
    export default {
        name: "Login.vue",
      data:function () {
        return{
          loginFlag:true,
          user:{
            userName:'',
            password:'',
            rePassword:'',
          },
          loginIconStaus:true,
          registIconStatus:false,
          showOrNot:'',
        }
      },
      methods:{
        switchLogin: function () {
          this.loginFlag=!this.loginFlag;
          this.showOrNot=!this.showOrNot;
        },
        login: function () {

        },
        regist: function () {

        }
      },
      beforeMount:function () {
        this.showOrNot="color:black"
      }
    }
</script>

<style scoped>

  .background{
    background: url(../../assets/imgs/photo_splash_signin_1141x759_v4.jpg);
    background-repeat: no-repeat;
    background-size: 100%;
    background-position: 0,-300px;
  }
  .header{
    background: rgba(0,0,0,0.98);
    height: 60px;
  }
  .header-left{
    font-size: 20px;
    font-weight: bold;
    line-height: 60px;
    text-align: center;
    width: 20%;
    float: left;
    color: beige;
    font-family: "monaco","Tahoma",onospace;
  }
  .iconfont{
    font-size: 20px;
  }
  .header-center{

  }
  .header-right{
    text-align: center;
    float: right;
    margin: 20px 50px;
    font-size: 20px;
    color: mediumslateblue;
    font-family:"monaco","Tahoma",onospace;
  }
  .body{
    height: 700px;
  }
  .middle{
    height: 700px;

    position: relative;
  }
  .middle-show{
    height: 400px;
    width: 600px;
    position:absolute;
    top:40%;
    left:10%;
  }
  #title{
    font-size: 50px;
    font-weight: 200;
    font-family: "monaco","Tahoma",onospace;
    color: white;
    opacity: 0.8;

  }
  .middle-regist{
    border: 1px solid cornflowerblue;
    border-radius: 4px;
    height: 400px;
    width: 360px;
    position: absolute;
    top:23%;
    right:22%;
    text-align: center;
    background: #eaeaea;
    opacity:0.9;
  }
  .regist{
    width: 100%;
    height: 100%;
  }
  .thead{
    height:50px;
    width:200px ;
  }
  .show{

  }
  .tr{
    height: 50px;
    border-bottom: 1px solid lightskyblue;
  }
  .td{
    font-weight: bold;
    color: rgba(133,133,133,0.69);
    font-size: 18px;
    line-height: 50px;
    width: 200px;
  }
  .td:hover{
    font-weight: bold;
    color: black;
    font-size: 18px;
    line-height: 50px;
    width: 200px;
  }
  .footer{
    height: 150px;
    background: aliceblue;
  }
  .input{
    background-color: white;
    font-size: 14px;
    border-radius: 4px;
    border: 1px solid cornflowerblue;
    font-family: "monaco","Tahoma",onospace;
    letter-spacing: 4px;
    width: 280px;
    height: 40px;
    padding-left: 20px;
  }
  .inputName{

    position: absolute;
    left: 0px;
    top: 0px;
    bottom: 0px;
    right: 0px;
    margin: 100px auto;

  }
  .inputPwd{
    position: absolute;
    left: 0px;
    top: 0px;
    bottom: 0px;
    right: 0px;
    margin: 160px auto;
  }
  .inputRePwd{
    position: absolute;
    left: 0px;
    top: 0px;
    bottom: 0px;
    right: 0px;
    margin: 220px auto;
  }
  .button{
     background-color: darkslateblue;
     font-size: 18px;
     font-weight: bold;
     color: white;
     border-radius: 4px;
     width: 300px;
     height: 40px;
     position: absolute;
     left: 0px;
     top: 0px;
     bottom: 0px;
     right: 0px;
     margin: 300px auto;
   }
  .button:hover{
    background-color: mediumslateblue;
  }
  .forget{
    font-size: 10px;
    position: absolute;
    bottom: 5%;
  }
</style>
