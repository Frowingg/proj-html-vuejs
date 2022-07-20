<template> 
    <div>
        <MyJumbotron />

        <MyRegisterArea />

        <MyNumberArea />

        <MyCoursesArea :infoCourses=infoCourses  
                       :infoInstructors=infoInstructors
        />

        <MySlider :infoSlider=infoSlider />

        <MyNews :infoNews=infoNews />

        <MyNewsLetter />

    </div>
</template>

<script>
import MyJumbotron from './MyJumbotron.vue';
import MyRegisterArea from './MyRegisterArea.vue';
import MyNumberArea from './MyNumberArea.vue';
import MyCoursesArea from './MyCoursesArea.vue';
import MySlider from './MySlider.vue';
import MyNews from './MyNews.vue';
import MyNewsLetter from './MyNewsLetter.vue';






export default {
    name: 'MyMain',
    components: {
        MyJumbotron,
        MyRegisterArea,
        MyNumberArea,
        MyCoursesArea,
        MySlider,
        MyNews,
        MyNewsLetter,

        
        },
    props: ['infoCourses', 'infoInstructors', 'infoSlider', 'infoNews']
           

}
</script>

<style lang="scss" scoped>

</style>