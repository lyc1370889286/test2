<template>
  <div>
    <p>hello</p>
    <button @click="toTest">跳转</button>
    <button @click="toLogin">登陆</button>
  </div>

</template>

<script>
export default {
  name: "home",
  methods:{
    toTest() {
      this.$router.push('/test');
    },

    toLogin() {
      this.$router.push('/login');
    }
  }
}
</script>

<style scoped>

</style>