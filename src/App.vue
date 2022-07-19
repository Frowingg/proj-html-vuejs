<template>
  <div id="app">

    <header>
        <MyHeader :infoHead= infoHeader />
    </header>

    <main>
        <MyMain :infoCour=infoCourses 
                :infoInstructo=infoInstructors
                :infoSlide= infoSlider 
                :infoNew=infoNews
        />
    </main>
    
    <footer>
      <MyFooter :footerConte=footerContent />
    </footer>

  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import MyFooter from './components/MyFooter.vue';


export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooter
  },
  data() {
    return{
      infoHeader: [
                    {
                      text: 'home',
                      tag: false
                    },
                    {
                      text: 'about',
                      tag: false
                    },
                    {
                      text: 'prices',
                      tag: false
                    },
                    {
                      text: 'courses',
                      tag: true,
                    },
                    {
                      text: 'locations',
                      tag: false
                    },
                    {
                      text: 'blog',
                      tag: false
                    },
                  ],
      infoCourses: [
                    {
                      img: 'courses-passplus-400x399',
                      text: 'Pass Plus'
                    },
                    {
                      img: 'course-intensive-400x399',
                      text: 'Intensive Course'
                    },
                    {
                      img: 'courses-instructor-400x400',
                      text: 'Instructors'
                    }
                  ],    
      infoInstructors: [
                        {
                          img : 'instructor-mikehart-600x381',
                          surname: 'Mike Hart'

                        },
                        {
                          img : 'instructor-johnsmith-600x381',
                          surname: 'Jhon Smith'
                        },
                        {
                          img : 'instructor-angelahart-600x381',
                          surname: 'Angela Hart'
                        }
                      ],  
      infoSlider: [
                    {
                      img: 'testimonial-sophia',
                      surname: 'Sophia Jones'
                    },
                    {
                      img: 'testimonial-grant',
                      surname: 'Grant'
                    },
                    {
                      img: 'testimonial-kate',
                      surname: 'Kate'
                    },
                    {
                      img: 'testimonial-harold',
                      isurnamemg: 'Harold'
                    },
                    {
                      img: 'testimonial-kelly',
                      surname:  'Kelly'
                    }
                  ],
      infoNews: [
                  {
                    title:'What Car to Start With?',
                    img: 'blog-choosecar-700x441',
                    comments: '0 comments',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing.'
                  },
                  {
                    title:'Avada Driving School Expanding',
                    img: 'blogpost-10and2-700x441',
                    comments: '0 comments',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing.'
                  }
                ],
      footerContent: [
                      {
                        logo: 'avada-drivers-logo-2x-200x39',
                        text: 'Avada Driving School is the right choice for experienced drivers looking for a refresher course, or the brand new driver wanting to pass first time.',                    
                        address: '12345 North Main Street, New York, NY 555555',
                        tel: '1.800.555.6789',
                        email_address: 'info@your-domain.com',
                        site_link: 'Theme-Fusion.com',                      
                        pass_plus_link: 'Pass_Plus',
                        intensive_course_link: 'Intensive Course',
                        automatic_link: 'Automatic',
                        instructor_training_link: 'Instructor Training',
                        footerImg: 'footer-ad-grid'
                      }
                     ]
    }
  }
}
</script>

<style lang="scss">
// @import url('https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700&display=swap');
@import './style/common.scss';

// APP
header{
  position: fixed;
  z-index: 3;
  width: 100%;
}

</style>
