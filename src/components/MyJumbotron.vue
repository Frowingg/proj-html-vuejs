<template>
    <section id="jumbotron">
        <div class="container">
            <h1>Drive with Avada</h1>
            <p>We offer the finest driving tuition money can buy</p>
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
#jumbotron{
    width: 100%;
    height: 600px;
    background-image: url('../assets/img/homepage-hero-background.jpg');
    background-size: cover;
    position: relative;
    top: -90px;
    .container{
        display: flex;
        flex-direction: column;
        justify-content:center;
        height: 100%;
        color: white;

        h1{
            font-size: 40px;
        }
        p{
            font-size: 20px;
        }
    }

    #squares{
        position: absolute;
        right: 0;
        top: 220px;
        z-index: 1;

        .square{
            width: 50px;
            height: 50px;
            background-color: white;
            margin-bottom: 5px;
            border-radius: 5px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: relative;
            cursor: pointer;

            i{
                font-size: 20px
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