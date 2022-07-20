<template>
    <section id="my-slider">
        <div class="container">
            
            <h2>Testimonials</h2>
            <p>Here's what our happy drivers had to say about services:</p>
            <img :src="require('../assets/img/'+infoSlider[currentElement].img+'.png')" alt="img">
            <p>Avada Driving School really helped build my confidence behind the 
                wheel and with driving in general, and they got me a first time pass! <br>
                <span>Higly recommended.</span>          
            </p>
            <p id="name">{{infoSlider[currentElement].surname}}</p>
            <ul>

                <li v-for="(teste, i) in infoSlider" :key="i" @click="showThisElement(i)">
                    <a href="#">
                        <div class="circle" :class="{'active-circle' : currentElement === i}"></div >
                    </a>
                </li>

            </ul>
            
        </div>

     </section>
</template>

<script>
export default {
    name: 'MySlider',
    props: ['infoSlider'],
    data() {
        return {
            currentElement: 0
        }
    },
    methods: {
        showThisElement(index) {
            this.currentElement = index;
        } 
    }
}
</script>

<style lang="scss" scoped>
#my-slider{
    padding: 80px 0;
    background-image: url('../assets/img/testimonial-background.jpg');
}
.container{
    width: 40%;
    text-align: center;
    padding: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
    
    h2{
        margin-bottom: 10px
    }
    p{
        margin-bottom: 25px;
        font-weight: 300;

    }
    img{
        width: 110px;
        margin-bottom: 25px;
    }
    #name{
        font-weight: 700;
        font-size: 15px
    }
    ul{
    list-style-type: none;
    display: flex;
    margin-top: 30px;
    }
    li{
    margin-left: 10px;
    }
    .circle{
        width: 10px;
        height: 10px;
        border: 1px solid gray;
        border-radius: 50%
    }
    .active-circle{
        background-color: gray;
    }
}
</style>