<template>
  <div >
    <form action="" class="login">
      <p>CSI语音技术吧</p>
      <input type="text" v-model="userName" placeholder="用户名">
      <input type="password" v-model="userPassword" placeholder="密码">
      <label><input type="checkbox" name="ten" id="yu">记住密码</label>
      <el-button type="submit" class="btn" @click="toLogin"> 登  录 </el-button>
      <el-button type="submit" class="btn btn1" @click="toRegister"> 注  册 </el-button>
    </form>
  </div>
</template>

<script>
// import {requestPost, requestGet} from "@/api/api";
import {login} from "@/api/api";

export default {
  name: "login",
  data() {
    return {
      msg: 'null',
      userName: '',
      userPassword: ''
    }
  },
  methods: {
    async toLogin() {
      let userInfo = {"username": this.userName, "password": this.userPassword};
      let judge = await login(userInfo);
      console.log(judge);
      console.log((judge.token))
      if (judge.result === "yes") {
        window.sessionStorage.setItem("token", judge.token);
        console.log("success!");
        await this.$router.push('/menu');
      } else {
        console.log("failed");
      }
    },

    toRegister() {
      this.$router.push('/register');
    }
  }
}
</script>

<style scoped>
*{
  user-select: none;
  /* 无法选中，整体感更强 */
}

body{
  background: url("./../../assets/wallpaper.jpg") no-repeat fixed;
}
#yu{
  margin-left: -544px;
  width: min-content;
  height: min-content;
}
.login{
  position: absolute;
  top: 50%;
  margin-top: -200px;
  left: 50%;
  margin-left: -200px;
  /* absolute居中的一种方法 */
  background-color: whitesmoke;
  width: 400px;
  height: 400px;
  border-radius: 25px;
  text-align: center;
  padding: 5px 40px;
  box-sizing: border-box;
  /* 这样padding就不会影响大小 */
}
p{
  font-size: 42px;
  font-weight: 600;
}

input{
  background-color: whitesmoke;
  width: 100%;
  height: 40px;
  margin-bottom: 10px;
  border: none;
  border-bottom: 2px solid silver;
  /* 下面的会覆盖上面的步伐 */
  outline: none;
  font-size: 22px;
}

.btn{
  display: block;
  background-color:#3399CC ;
  width: 42%;
  height: 52px;
  border-radius: 23px;
  margin-top: 40px;
  font-size: 31px;
  font-weight: 600;
  color: white;
  float:left;
}
.btn1
{
  margin-left: 40px;
}
.btn:hover{
  background-color:#17D3AD
}
</style>