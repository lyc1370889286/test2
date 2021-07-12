<template>

  <div >
    <form action="" class="login">
      <p>邮箱验证</p >
      <input type="text" placeholder="邮箱验证码">


      <el-button type="submit" class="btn" @click="func1"> 验证 </el-button>

    </form>
  </div>
</template>

<script>
//import {request} from "@/api/api";

export default {
  name: "emailCheck",
  methods: {
    func1() {
      alert("check")
    }
  }
}
</script>

<style scoped>
*{
  user-select: none;
  /* 无法选中，整体感更强 */
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
  margin-left: 88px;
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