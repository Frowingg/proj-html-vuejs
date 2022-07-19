<template>

  <section id="my-news">
      <div class="container">
          <div class="card-base">

              <h2>Latest News</h2>
            
              <div class="news-content">

                  <div class="news-card" v-for="(singleInfo, i) in infoNe" :key="i">
                      <img :src="require('../assets/img/'+singleInfo.img+'.jpg')" alt="">
                      <div class="title">{{singleInfo.title}}</div>
                      <div class="date">Febr 7th | <span>0 comments</span></div>
                      <p>Lorem ipsum dolor sit amet consectetur adipisicing.</p>
                  </div>
              </div>

              <button class="btn">MORE FROM THE BLOG</button>

          </div>

          
          <img id="border-bottom" src="../assets/img/latestnews-bottom-1200x105.png" alt="lt-bottom">

      </div>
  </section>

</template>

<script>
export default {
    name: 'MyNews',
    props: ['infoNe']
}
</script>

<style lang="scss" scoped>
#my-news{
  background-image: url(../assets/img/latestnews-background.jpg);
  background-size:cover;
}
#border-bottom{
    width: 100%;
    position: relative;
    top: -30px;
    left: 5px
}
.card-base{
  width: 100%;
  border-color: #799aae;
  border-bottom-left-radius:0px;
  border-bottom-right-radius:0px;
  position: relative;
  top: -30px;
  .news-content{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    padding: 30px;
    .news-card{
      width: 48%;
      // padding: 40px;

      img{
        width: 100%;
      }
      .title{
        color: #7abc64;
        font-weight: 700;
        margin: 10px 0;
      }
      .date{
        font-size: 10px;
        margin-bottom: 20px;

        span{
          color: #7abc64;
          font-size: 9px;
        }
      }
      p{
        font-size: 14px;
        font-weight: 300
      }
  }

  }
  
}
</style>