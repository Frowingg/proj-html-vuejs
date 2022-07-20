<template>
    <section id="jumbotron">
        <div class="container">
            <div id="header-content">
                <h1>Drive with Avada</h1>
                <p>We offer the finest driving tuition money can buy</p>
            </div>
        </div>

        <div id="squares">
            <div class="square">
                <i class="fa-solid fa-folder-plus"></i>
                <p>Demos</p>
            </div>

            <div class="square">
                <i id="dollar" class="fa-solid fa-dollar-sign"></i>
                <p id="num">39</p>
                <p>On sale</p>
            </div>
        </div>
    </section>
  
</template>

<script>
export default {
    name: 'MyJumbotron'
}
</script>

<style lang="scss" scoped>
@import '../style/variable.scss';
#jumbotron{
    width: 100%;
    height: 600px;
    background-image: url('../assets/img/homepage-hero-background.jpg');
    background-size:cover;
    background-attachment:fixed;
    background-position:-150px;
    position: relative;
    top: -90px;
    .container{
        display: flex;
        flex-direction: column;
        justify-content:center;
        height: 100%;
        color: white;
        position: relative;

        #header-content{
            position: relative;
            top: 90px
        }
        h1{
            font-size: 40px;
        }
        p{
            font-size: 20px;
        }
    }

    #squares{
        right: 0;
        top: 100px;
        z-index: 3;
        position: fixed;

        .square{
            width: 50px;
            height: 50px;
            background-color: #f3f3f3;
            margin-right: 10px;
            margin-bottom: 5px;
            border-radius: 5px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: relative;
            cursor: pointer;

            i{
                font-size: 20px;
                color: $brand_title_color
            }

            p{
                font-size: 11px;
            }

            #num{
                color: green;
                font-size: 25px;
                font-weight: 900;
            }
            
            #dollar{
                color: green;
                position: absolute;
                font-weight: 900;
                font-size: 11px;
                top: 5px;
                left: 5px
            }
        }
    }
}
</style>