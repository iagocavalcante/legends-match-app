<template>
  <Page>
    <Login/>
  </Page>
</template>

<script >
  import Login from '~/views/Login'
  export default {
    components: {
      Login
    },
    data() {
      return {
        msg: 'Hello World!'
      }
    }
  }
</script>

<style scoped>
  ActionBar {
    background-color: #53ba82;
    color: #ffffff;
  }

  .message {
    vertical-align: center;
    text-align: center;
    font-size: 20;
    color: #333333;
  }
</style>
