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

// BASE
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

// COMMON
.card-base{
    width: 280px;
    height: 280px;
    background-color: white;
    border-radius: 15px;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    margin: 0 5px;
    
    border-top: 6px solid #7abc64;
}

.container{
  width: 60%;
  margin: 0 auto;
}

.btn{
  background-color: #7abc64;
  color: white;
  border: none;
  padding: 10px 15px;
  border-radius: 30px;
  font-weight: 900;
  font-size: 11px;
}

// APP
header{
  position: fixed;
  z-index: 2;
  width: 100%;
}

// TEMP
body{
  height: 4000px;
  color: gray;
}
</style>
