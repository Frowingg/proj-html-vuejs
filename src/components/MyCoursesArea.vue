<template>
    <div class="container">
        <section id="courses-area">
            
                <section id="courses-info">

                    <div id="courses-info-left">
                        <div class="card-base">
                            <img src="../assets/img/new-corner.jpg" alt="img">
                            <h2>Courses</h2>
                            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Alias quod necessitatibus error eos voluptates eveniet, numquam exercitationem aspernatur suscipit iusto.</p>
                            <button class="btn">COURSE INFORMATION</button>
                        </div>
                    </div>

                    <div id="courses-info-right">

                        <div class="img-card" v-for="(singleInfo, i) in infoCou" :key="i">
                            <img :src="require('../assets/img/'+singleInfo.img+'.jpg')" alt="img">
                            <p>{{singleInfo.text}}</p>
                            <button class="lm">LEARN MORE</button>
                        </div>

                    </div>

                </section>

                <section id="courses-per">

                        <div class="card-base">
                            <div class="circle">
                                95%
                            </div>
                            <p>PASS RATE</p>
                        </div>
                        <div class="card-base">
                            <div class="circle">
                            100%
                                
                            </div>
                            <p>REFERRAL RATE</p>                    
                        </div>
                        <div class="card-base">
                            <div class="circle">
                                0%
                                
                            </div>
                            <p>ACCIDENT RATE</p>                    
                        </div>

                </section>

                <section id="instructors-area">
                    <MyInstructorArea :infoInst=infoInstru />
                </section>
        </section>
    </div>
</template>

<script>
import MyInstructorArea from './MyInstructorArea.vue';

export default {
    name: 'MyCoursesArea',
    props: ['infoCou','infoInstru'],
    components: {
        MyInstructorArea,
    },
    
}
</script>

<style lang="scss" scoped>
@import '../style/variable.scss';

#courses-info{
    padding: 50px 0;
    display: flex;

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
            color: #3e3e3e;
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
            color: #7497aa;
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

#courses-per {
    flex-direction: row;
    .card-base{
        width: calc(100% / 3);
        padding: 50px;
        display: flex;
        flex-direction: column;
    }
    .square-per{
        width: calc(100% / 3);
        height: 280px;
        margin: 0 5px;
        padding: 55px;
    }
    .circle{
        width: 100%;
        height: 100%;
        border-radius: 50%;
        border: 8px solid #7abc7a;
        font-size: 40px;
        display: flex;
        flex-direction: column;

    }
    p{
        font-size: 14px;
        position: relative;
        top: 30px
    }

}
</style>