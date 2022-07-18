<template> 
    <div>
        <MyJumbotron />

        <MyRegisterArea />

        <MyNumberArea />

        <MyCoursesArea :infoCou=infoCour 
                       :infoInstru=infoInstructo
        />

        <MySlider />

    </div>
</template>

<script>
import MyJumbotron from './MyJumbotron.vue';
import MyRegisterArea from './MyRegisterArea.vue';
import MyNumberArea from './MyNumberArea.vue';
import MyCoursesArea from './MyCoursesArea.vue';
import MySlider from './MySlider.vue';




export default {
    name: 'MyMain',
    components: {
        MyJumbotron,
        MyRegisterArea,
        MyNumberArea,
        MyCoursesArea,
        MySlider,
        
        },
    props: ( ['infoCour'], ['infoInstructo'] )
           

}
</script>

<style lang="scss" scoped>

</style>