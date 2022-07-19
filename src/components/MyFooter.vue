<template>
    <footer>
        
        <section id="footer-top">
            <div class="container" v-for="(infoFoot, i) in footerConte" :key="i">

                <div class="col" >
                    <img :src="require('../assets/img/'+infoFoot.logo+'.png')" alt="logo-img">
                    <p>{{infoFoot.text}}</p>                   
                </div>

                <div class="col">
                    <h3>CONTACT DETAILS</h3>
                    <ul id="info">
                        <li>
                            <i class="fa-solid fa-house-chimney"></i><p> {{infoFoot.address}}</p>
                        </li>
                        <li>
                            <i class="fa-solid fa-phone"></i><p>{{infoFoot.tel}}</p>
                        </li>
                        <li>
                            <i class="fa-solid fa-envelope"></i> <a href="#">{{infoFoot.email_address}}</a>
                        </li>
                        <li>
                            <i class="fa-solid fa-link"></i> <a href="#">{{infoFoot.site_link}}</a>
                        </li>
                    </ul>
                </div>

                <div class="col">
                    <h3>COURSES</h3>
                    <ul id="courses">
                        <li>
                            <i class="fa-solid fa-circle-right"></i><a href="#">{{infoFoot.pass_plus_link}}</a>
                        </li>
                        <li>
                            <i class="fa-solid fa-circle-right"></i><a href="#">{{infoFoot.intensive_course_link}}</a>
                        </li>
                        <li>
                            <i class="fa-solid fa-circle-right"></i><a href="#">{{infoFoot.automatic_link}}</a>
                        </li>
                        <li>
                            <i class="fa-solid fa-circle-right"></i><a href="#">{{infoFoot.instructor_training_link}}</a>
                        </li>
                    </ul>
                </div>
                <div class="col">
                    <img :src="require('../assets/img/'+infoFoot.footerImg+'.png')" alt="img">
                    <button class="btn">BOOK NOW</button>
                </div>
            </div>
        </section>

        <section id="footer-bottom">
            <div class="container">
                <div id="fb-left">
                    <p>© Copyright 2012 - 2022 | Avada Theme by <a href="#">ThemeFusion</a> | All Rights Reserved | Powered by <a href="#">WordPress</a></p>
                </div>
                <div id="fb-right">
                    <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                    <a href="#"><i class="fa-brands fa-twitter"></i></a>
                    <a href="#"><i class="fa-brands fa-youtube"></i></a>
                    <a href="#"><i class="fa-brands fa-instagram"></i></a>
                </div>
            </div>
        </section>    

    </footer>
</template>

<script>
export default {
    name: 'MyFooter',
    props: ['footerConte']
}
</script>

<style lang="scss" scoped>
.container{
    display: flex;
    justify-content: space-between;
}
p{
    color: white;
    font-size: 10px;
    line-height: 20px;
}
i{
    margin-right: 15px;
    font-size: 13px;
}
a{
    color: white;
    font-size: 10px;
    text-decoration: none;
}
.container .col:nth-child(4){
    display: flex;
    flex-direction: column;
    align-items: center;
    .btn{
        margin-top: 20px
    }
}

#footer-top{
    background-image: url(../assets/img/footer-background-color.jpg);
    padding: 50px 0;

    .col{
        width: calc(100% / 4);
        margin: 0 13px;

        #courses, #info{
            list-style-type: none;
            display: flex;
            flex-direction: column;
        }
        #courses li a, #courses li i{
            font-size: 13px;
            color: #7abc64;
        }
        img{
            width: 100%
        }
        h3{
            color: white;
            font-size: 12px;
            margin-bottom: 20px
        }
        li{
            display: flex;
            align-items: flex-start;
            margin-bottom: 10px;
        }
        
    }
}

#footer-bottom{
    background-color: #1c1d1e;
    padding: 40px 0;
    
    #fb-left{
        a{
            color: #7abc64;
        }
    }
}

</style>