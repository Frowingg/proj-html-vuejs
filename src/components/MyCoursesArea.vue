<template>
    <section id="courses-area">
        <div class="container">
            <section id="courses-info">

                <div id="courses-info-left">
                    <div class="course-card">
                        <h2>Courses</h2>
                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Alias quod necessitatibus error eos voluptates eveniet, numquam exercitationem aspernatur suscipit iusto.</p>
                        <button class="btn">COURSE INFORMATION</button>
                    </div>
                </div>

                <div id="courses-info-right">
                    <div class="img-card">
                        <div class="img"></div>
                        <p>Pass Plus</p>
                        <button class="lm">LEARN MORE</button>
                    </div>

                    <div class="img-card">
                        <div class="img"></div>
                        <p>Intensive Course</p>
                        <button class="lm">LEARN MORE</button>
                        
                    </div>

                    <div class="img-card">
                        <div class="img"></div>
                        <p>Instructors</p>
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

        </div>
    </section>
</template>

<script>
export default {
    name: 'MyCoursesArea'
}
</script>

<style lang="scss" scoped>
#courses-info{
    padding: 50px 0;
    display: flex;

    #courses-info-left{
        text-align: center;
        display: flex;
        justify-content: space-between;
        width: 40%;
        padding: 30px;
        box-shadow: 10px 10px 5px grey;
        position: relative;
        bottom: 85px;
        background-color: white;
        border-radius: 15px;

        h2{
            color: black;
            font-size: 30px;
        }
        p{
            font-size: 12px;
            line-height: 30px;
            margin: 20px 0;
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
        .img{
            width: 100%;
            height: 60%;
            background-color: blue;
            margin-bottom: 15px;
        }
        p{
            color: #7497aa;
            margin-bottom: 10px;
        }
        .lm{
            width: fit-content;
            margin: 0 auto;
            padding: 5px 10px;
            border-radius: 25px;
            border: 1px solid #7497aa;
            color: #7497aa;
            font-size: 10px;
            background-color: white;
        }
        .lm:hover{
            color: #97b27b;
            border:2px solid #97b27b;
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
        background-color: pink;
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