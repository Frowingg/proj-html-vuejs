<template>

  <section id="my-news">
      <div class="container">
          <div class="card-base">

              <h2>Latest News</h2>
            
              <div class="news-content">

                  <div class="news-card" v-for="(singleInfo, i) in infoNews" :key="i">
                      <img :src="require('../assets/img/'+singleInfo.img+'.jpg')" alt="">
                      <div class="title">{{singleInfo.title}}</div>
                      <div class="date">{{singleInfo.date}} <span>|</span> <span>{{singleInfo.comments}}</span></div>
                      <p>{{singleInfo.text}}</p>
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
    props: ['infoNews']
}
</script>

<style lang="scss" scoped>
@import '../style/variable.scss';

#my-news{
  background-image: url(../assets/img/latestnews-background.jpg);
  background-size:cover;
}
#border-bottom{
    width: 100%;
    position: relative;
    top: -30px;
    left: 6px
}
.card-base{
  width: 100%;
  border-color: #799aae;
  border-bottom-left-radius:0px;
  border-bottom-right-radius:0px;
  position: relative;
  top: -30px;
  h2{
    color: $brand_title_color;
  }
  .news-content{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    padding: 30px;
    .news-card{
      width: 48%;
      img{
        width: 100%;
      }
      .title{
        color: $brand_main_color;
        font-weight: 700;
        margin: 10px 0;
      }
      .date span:first-child{
        margin: 0 3px;
      }
      .date{
        font-size: 10px;
        margin-bottom: 20px;

        span{
          color: $brand_main_color;
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