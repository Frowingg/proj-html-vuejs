<template> 
    <div>
        <MyJumbotron />

        <MyRegisterArea />

        <MyNumberArea />

    </div>
</template>

<script>
import MyJumbotron from './MyJumbotron.vue';
import MyRegisterArea from './MyRegisterArea.vue';
import MyNumberArea from './MyNumberArea.vue';


export default {
    name: 'MyMain',
    components: {
        MyJumbotron,
        MyRegisterArea,
        MyNumberArea
    }

}
</script>

<style lang="scss" scoped>

</style>