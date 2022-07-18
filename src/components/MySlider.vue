<template>
    <section id="my-slider">

        <div class="container">
            <h2>Testimonials</h2>
            <p>Here's what our happy drivers had to say about services:</p>
            <img src="" alt="">
            <p></p>
            <p></p>
            <ul>
                <li>
                    <div class="dot"></div>
                </li>
            </ul>
        </div>

     </section>
</template>

<script>
export default {
    name: 'MySlider',
}
</script>

<style lang="scss" scoped>
#my-slider{
    background-color: red;
    padding: 80px 0;
}
.container{
    width: 40%;
    height: 400px;
    background-color: blue;
    text-align: center;
    padding: 30px;
    
    h2{
        margin-bottom: 10px
    }
    p{
        margin-bottom: 25px

    }
}
</style>