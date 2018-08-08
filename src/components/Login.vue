<template>
  <div>
    <h1>用户登录</h1>
    <input type="text" placeholder="用户名">
    <input type="password" placeholder="密码">
    <input type="button" value="提交" v-on:click="doLogin">
  </div>
</template>

<script>
    export default {
        name: "login",
        data(){
          return{
            username:'',
            password:'',
          }
        },
        methods:{
          doLogin:function(){
              // 向后台发送ajax请求
              this.$axios.request({
                url: 'http://127.0.0.1:8000/api/v1/auth/',
                method: 'POST',
                emulateJSON:'true',
                data:{
                  user:this.username,
                  pwd:this.password,
                },
                headers:{
                  'Content-Type:':'application/json'
                },
                responseType: 'json'
              }).then(function (arg) {
                // 成功之后
                console.log(123);
              }).catch(function (arg) {

              })
          }
        }
    }
</script>

<style scoped>

</style>
