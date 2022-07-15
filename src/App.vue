<template>
  <div id="app">

    <header>
        <MyHeader :info = "infoHeader" />
    </header>

    <main>
        <MyMain />
    </main>
    
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain
  },
  data() {
    return{
      infoHeader: [
                    {
                      text: 'home'
                    },
                    {
                      text: 'about'
                    },
                    {
                      text: 'prices'
                    },
                    {
                      text: 'courses'
                    },
                    {
                      text: 'locations'
                    },
                    {
                      text: 'blog'
                    },
                  ]
    }
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  height: 1000px;
}
header{
  position: fixed;
  z-index: 2;
  width: 100%;
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
