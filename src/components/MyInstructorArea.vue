<template>
        <section id="instructor-area">

            <div id="instructor-area-top">
                <div id="title">
                    <h2>Your Instructors</h2>
                </div>
                <div id="my-content">
                    <div id="text">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad fugit recusandae iusto magnam suscipit tempora debitis aperiam, perferendis voluptates.
                    </div>
                    <div id="button">
                        <button class="btn">
                            MORE ABOUT US
                        </button>
                    </div>
                </div>
            </div>

            <div id="instructor-area-bottom">
                
                <div class="card-base" v-for="(singleInfo,i) in infoInst" :key="i">
                    <img :src="require('../assets/img/'+singleInfo.img+'.jpg')" alt="img">
                    <div class="info">
                        <h3>{{singleInfo.surname}}</h3>
                        <div class="icons">
                            <i class="fa-brands fa-facebook-f"></i>
                            <i class="fa-brands fa-twitter"></i>
                            <i class="fa-brands fa-instagram"></i>
                        </div>
                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. </p>
                    </div>                   
                </div>
                
            </div>

        </section>
</template>

<script>
export default {
    name: 'MyInstructorArea',
    props: ['infoInst']
}
</script>

<style lang="scss" scoped>
.card-base:hover img{
            box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;;
        }
#instructor-area{

    #instructor-area-top{
        margin: 100px 0 60px;
        font-size: 18px;

        #title{
            margin-bottom: 30px;
        }

        #my-content{
            display: flex;
            justify-content: space-between;

            #text{
                width: 66%;
                font-size: 15px;
                line-height: 30px;
            }
            
            #button{
                width: 30%;

                .btn{
                    width: 100%;
                }
            }
        }
    }
    
    #instructor-area-bottom div:nth-child(2) {
            height: 350px;
        }
    
    #instructor-area-bottom{
        display: flex;

        .card-base{
            height: 340px;
            padding: 30px;
            text-align: center;

        
            img{
                width: 100%;
                margin-bottom: 25px;
            }
            .info{
                height: fit-content;  
                
                h3{
                    color: black;

                }
                

                .icons{
                    margin: 7.5px 0;
                    height: min-content;

                    i{
                        margin: 0 7.5px;
                        font-size: 13px;
                    }
                    
                }
                p{
                    line-height: 22px;
                    font-size: 12px
                }
            }
        }
    }
    
}

</style>