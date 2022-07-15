<template>
  <div id="app">
    <MyHeader />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';

export default {
  name: 'App',
  components: {
    MyHeader
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.container{
  width: 60%;
  margin: 0 auto;
}
.btn{
  background-color: #97b27b;
  color: white;
  border: none;
  padding: 10px 15px;
  border-radius: 30px;
  font-weight: 900;
  font-size: 11px;
}
</style>
