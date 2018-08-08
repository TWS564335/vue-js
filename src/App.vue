<template>
  <div id="app">
    <img src="">
    <router-link to="/">首页</router-link>
    <router-link to="/Course">课程</router-link>
    <router-link to="/News">深科技</router-link>
    <router-link to="/login">登陆</router-link>

    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>

</style>
