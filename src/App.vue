<template>
  <div id="app">

    <header>
        <MyHeader :infoHead= infoHeader />
    </header>

    <main>
        <MyMain :infoCour=infoCourses 
                :infoInstructo=infoInstructors
                :infoSlide= infoSlider />
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
                  ],
      infoCourses: [
                    {
                      image: 'courses-passplus-400x399.jpg',
                      text: 'Pass Plus'
                    },
                    {
                      image: 'course-intensive-400x399.jpg',
                      text: 'Intensive Course'
                    },
                    {
                      image: 'courses-instructor-400x400.jpg',
                      text: 'Instructors'
                    }
                  ],    
      infoInstructors: [
                        {
                          image : 'instructor-mikehart-600x381',
                          surname: 'Mike Hart'

                        },
                        {
                          image : 'instructor-johnsmith-600x381',
                          surname: 'Jhon Smith'
                        },
                        {
                          image : 'instructor-angelahart-600x381',
                          surname: 'Angela Hart'
                        }
                      ],  
      infoSlider: [
                    {
                      image: 'testimonial-sophia',
                      surname: 'Sophia Jones'
                    },
                    {
                      image: 'testimonial-grant',
                      surname: 'Grant'
                    },
                    {
                      image: 'testimonial-kate',
                      surname: 'Kate'
                    },
                    {
                      image: 'testimonial-harold',
                      isurnamemg: 'Harold'
                    },
                    {
                      image: 'testimonial-kelly',
                      surname:  'Kelly'
                    }
                  ],
    }
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700&display=swap');

// BASE
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  font-family: 'Lato', sans-serif;
}

// COMMON
.card-base{
    width: 280px;
    min-height: 280px;
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
  cursor: pointer;
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
