<template>
  <header>

    <div class="header-top">
        <div class="container">
            <div>We have a 95% Successful Pass Rate!</div>
            <div><i class="fa-solid fa-phone-flip"></i>Give us a call to book your tuition! 1-800-555-555</div>
        </div>
    </div>

    <div class="header-bottom">
      <div class="container">

          <img src="../assets/img/avada-drivers-logo-2x-200x39.png" alt="">

          <div class="left-header-bottom">
            
              <nav>
                <ul>
                  <li v-for="(singleInfo, i) in infoHead" :key="i" :class="{'active-nav' : currentElement === i}">
                      {{singleInfo.text.toUpperCase()}} 
                      <div class="tag" :class="{'active-tag': singleInfo.tag}">NEW</div>
                  </li>
                </ul>
              </nav>

              <button class="btn">
                BOOK NOW
              </button>
          </div>
      </div>
    </div>

  </header>
</template>

<script>
export default {
  name: 'MyHeader',
  props: ['infoHead'],
  data() {
    return{
      currentElement: 0
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../style/variable.scss';

.container{
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.header-top{
  display: flex;
  background-color: #484848;
  color: #d6c9b0;
  height: 30px;
  font-size: 9px;

  i{
    margin-right: 10px;
  }
}

.header-bottom{
    display: flex;
    height: 90px;
    background-color: rgba(0,0,0,0.3);

    .left-header-bottom{
        display: flex;

        ul{
            display: flex;

            li{
                cursor: pointer;
                margin-right: 20px;
                color: white;
                font-size: 11px;
                font-weight: 900;
                height: 30px;
                display: flex;
                align-items: center;
            }
            .active-nav{
              color: $brand_main_color;
              border-bottom: 3px solid $brand_main_color;
            }
            li:hover{
                color: $brand_main_color;
                border-bottom: 3px solid $brand_main_color;
            }
          }

        .tag{
          display: none;
          font-size: 7px;
          font-weight: 900;
          color: white;
          background-color: $brand_main_color;
          height: min-content;
          padding: 4px;
          position: relative;
          right: -7px;
          top:1px;
        }
        .active-tag{
          display: block;
        }
    }
}
</style>