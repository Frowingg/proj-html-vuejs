<template> 
    <div>
        <MyJumbotron />

        <MyRegisterArea />

        <MyNumberArea />

        <MyCoursesArea />

        

    </div>
</template>

<script>
import MyJumbotron from './MyJumbotron.vue';
import MyRegisterArea from './MyRegisterArea.vue';
import MyNumberArea from './MyNumberArea.vue';
import MyCoursesArea from './MyCoursesArea.vue';



export default {
    name: 'MyMain',
    components: {
        MyJumbotron,
        MyRegisterArea,
        MyNumberArea,
        MyCoursesArea,
        }

}
</script>

<style lang="scss" scoped>

</style>