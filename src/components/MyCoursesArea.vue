<template>
    
        <section id="courses-area">
                
                <!-- COURSES INFO -->
                <section id="courses-info">
                    <div class="container">
                        <div id="courses-info-left">
                            <div class="card-base">
                                <img src="../assets/img/new-corner.jpg" alt="img">
                                <h2>Courses</h2>
                                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Alias quod necessitatibus error eos voluptates eveniet, numquam exercitationem aspernatur suscipit iusto.</p>
                                <button class="btn">COURSE INFORMATION</button>
                            </div>
                        </div>                  

                        <div id="courses-info-right">
                            <div class="img-card" v-for="(singleInfo, i) in infoCourses " :key="i">
                                <img :src="require('../assets/img/'+singleInfo.img+'.jpg')" alt="img">
                                <p>{{singleInfo.text}}</p>
                                <button class="lm">LEARN MORE</button>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- COURSES PERCENTAGE -->
                <section id="courses-per">

                        <div class="card-base">
                            <div class="box">
                                <div class="percent">
                                    <svg>
                                        <circle cx="70" cy="70" r="70"></circle>
                                        <circle cx="70" cy="70" r="70"></circle>
                                    </svg>
                                    <div class="number">
                                        <h2>95 <span>%</span> </h2>
                                    </div>
                                </div>
                                <h2 class="text">PASS RATE</h2>
                            </div>
                        </div>
                        <div class="card-base">
                            <div class="box">
                                <div class="percent">
                                    <svg>
                                        <circle cx="70" cy="70" r="70"></circle>
                                        <circle cx="70" cy="70" r="70"></circle>
                                    </svg>
                                    <div class="number">
                                        <h2>100 <span>%</span> </h2>
                                    </div>
                                </div>
                                <h2 class="text">REFERRAL RATE</h2>
                            </div>
                        </div>
                        <div class="card-base">
                            <div class="box">
                                <div class="percent">
                                    <svg>
                                        <circle cx="70" cy="70" r="70"></circle>
                                        <circle cx="70" cy="70" r="70"></circle>
                                    </svg>
                                    <div class="number">
                                        <h2>0 <span>%</span> </h2>
                                    </div>
                                </div>
                                <h2 class="text">ACCIDENT RATE</h2>
                            </div>
                        </div>

                </section>

                <section id="instructors-area">
                    <MyInstructorArea :infoInstructors=infoInstructors />
                </section>
        </section>
    
</template>

<script>
import MyInstructorArea from './MyInstructorArea.vue';

export default {
    name: 'MyCoursesArea',
    props: ['infoCourses','infoInstructors'],
    components: {
        MyInstructorArea,
    },
    
}
</script>

<style lang="scss" scoped>
@import '../style/variable.scss';
.container{
    display: flex;
}
#courses-info{
    padding: 50px 0;
    background-image: url('../assets/img/promise-background.jpg');
    background-size: cover;
    background-repeat: no-repeat;

    #courses-info-left{
        width: 40%;
        text-align: center;
        position: relative;
        bottom: 75px;

        .card-base{
            border-top: none;
            padding: 30px;
            width: 100%;
            position: relative;

            img{
                position: absolute;
                width: 55px;
                top: 0;
                left: 0;
                border-top-left-radius: 15px;
            }

        }
        h2{
            color: $brand_title_color;
            font-size: 30px;
        }
        p{
            font-size: 12px;
            line-height: 25px;
            margin: 20px 0;
            font-weight: 300;
        }
    }

    #courses-info-right{
        width: 60%;
        display: flex;
        margin-left: 20px;

        .img-card{
            width: calc(100% / 3);
            height: 200px;
            margin: 0 15px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        img{
            width: 100%;
            height: 60%;
            margin-bottom: 15px;
        }
        p{
            color: $brand_text_color;
            margin-bottom: 10px;
        }
        .lm{
            width: fit-content;
            margin: 0 auto;
            padding: 7px 13px;
            border-radius: 25px;
            border: 2px solid $brand_text_color;
            color: $brand_text_color;
            font-size: 10px;
            background-color: white;
            cursor: pointer;
        }
        .lm:hover{
            color: $brand_main_color;
            border:2px solid $brand_main_color;
        }
    }
}

// COURSES PERCENTAGE
#courses-per, #courses-per *{
    display: flex;
    align-items: center;
    justify-content: center;
}

#courses-per .card-base:nth-child(2) .box .percent svg circle:nth-child(2){
    stroke-dashoffset: calc(440 - (440 * 100)/ 100);
}
#courses-per .card-base:nth-child(3) .box .percent svg circle:nth-child(2){
        stroke-dashoffset: calc(440 - (440 * 1)/ 100);
    }
#courses-per {
    .box{
        position: relative;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        background: white;
    }
    .box .percent{
        position: relative;
        width: 150px;
        height: 150px;
    }
    .box .percent svg{
        position: relative;
        width: 150px;
        height: 150px;
    }
    .box .percent svg circle{
        width: 150px;
        height: 150px;
        fill: none;
        stroke-width: 7;
        stroke: #000;
        transform: translate(5px,5px);
        stroke-dasharray: 440;
        stroke-dashoffset: 440;
        stroke-linecap: round;
    }
    .box .percent svg circle:nth-child(1){
        stroke-dashoffset: 0;
        stroke: #f3f3f3;
    }
    .box .percent svg circle:nth-child(2){
        stroke-dashoffset: calc(440 - (440 * 95)/ 100);
        stroke: $brand_main_color;
    }
    .box .percent .number{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .box .percent .number h2{
        font-size: 35px;
        font-weight: 400;
    }
    .box .percent .number h2 span{
        font-size: 24px;
    }
    .box .text{
        padding: 10px 0 0;
        font-weight: 700;
        letter-spacing: 1px;
        font-size: 12px;
    }
}
</style>