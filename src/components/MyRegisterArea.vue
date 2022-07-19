<template>
    <section id="Register-area">
        <div class="container">

            <div class="reg" id="left-reg">
            
                <h2>Get Behind The Wheel</h2>

                <p id="sub-title">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    Modi quaerat laudantium libero omnis. Sit error nesciunt,
                    id minus temporibus sint! Porro, impedit labore unde.
                </p>

                <p id="txt">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitatio
                    aspernatur deleniti enim molestiae vitae. Officiis aperiam ab placeat 
                    reprehenderit assumenda ullam, unde in ex accusantium reiciendis tenetur 
                    fugiat, saepe officia? Lorem ipsum dolor sit amet, consectetur adipisicing 
                    elit. Accusantium quidem aliquid fuga ipsum reiciendis.
                </p>

            </div>

            <div class="card-base" id="right-reg">
                <h3>First Lesson Free!</h3>
                <p>When you make a block booking with us your first lesson is included free.</p>

                <div class="input-area">
                    <input type="text" placeholder="Your Name*">
                    <input type="email" placeholder="Email*">
                    <input type="tel" placeholder="Telephone">
                    <input type="text" placeholder="Location">
                </div>

                <button class="btn">
                    REQUEST A CALLBACK
                </button>

            </div>

        </div>
    </section>  
</template>

<script>
export default {
    name: 'MyRegisterArea'
}
</script>

<style lang="scss" scoped>
@import '../style/variable.scss';
.container{
    display: flex;
}
.card-base{
    width: 50%;
}
#left-reg{
    width: 50%;
    padding-right: 20px;
    h2{
        margin: 20px 0;
        color: $brand_title_color;
    }
    #sub-title{
        line-height: 25px;
        margin-bottom: 30px;
        font-weight: 300;
    }
    #txt{
        font-size: 13px;
        line-height: 20px;
        font-weight: 300;
    }
}

#right-reg{
    position: relative;
    bottom: 115px;

    h3{
        color: $brand_main_color;
        font-size: 24px;
    }

    p{
        margin: 40px 0;
        font-size: 13px;
        font-weight: 300;
    }
    
    .input-area{
        display: flex;
        flex-direction: column;

        font-weight: 300;
    }
    .input-area *{ 
        margin-bottom: 20px;
        padding: 8px;
        border-radius: 5px;
        background-color: #f7f7f7;

        font-weight: 300;
    }
}
</style>