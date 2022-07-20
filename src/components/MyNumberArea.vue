<template>
  <section id="Number-area">
    <div class="container">
        <div id="left-number-area">
            <h2>Start Learning to Drive Today</h2>
            <p>Give us a call to shedule your first driving lesson</p>
        </div>
        <div id="right-number-area">
            <p><i class="fa-solid fa-phone-flip"></i>1-800-555-555</p>
        </div>

    </div>
  </section>
</template>

<script>
export default {
    name: 'MyNumberArea'
}
</script>

<style lang="scss" scoped>
@import '../style/variable.scss';

#Number-area{
    background-image: url('../assets/img/horizontal-cta-background.jpg');
    background-size:cover;
    color: white;
    padding: 60px 0;

    .container{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
    }
    

}
#left-number-area{
    h2{
        font-size: 30px;
        margin-bottom: 5px
    }
}

#right-number-area{
    i{
        margin-right: 25px;
    }
    p{
        font-size: 25px;
        margin-right:40px
    }
}
</style>