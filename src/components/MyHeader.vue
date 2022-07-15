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
                  <li>HOME</li>
                  <li>ABOUT</li>
                  <li>PRICES</li>
                  <li>COURSES</li> <span class="tag">NEW</span>
                  <li>LOCATIONS</li>
                  <li>BLOG</li>
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

}
</script>

<style lang="scss" scoped>
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
    background-color: rgba(0,0,0,0.2);

    .left-header-bottom{
        display: flex;

        ul{
            list-style-type: none;
            display: flex;

            li{
                margin-right: 20px;
                color: white;
                font-size: 11px;
                font-weight: 900;
                height: 30px;
                display: flex;
                align-items: center;
            }
            li:hover{
                color: #97b27b;
                border-bottom: 3px solid #97b27b;
            }
          }

        .tag{
          font-size: 7px;
          font-weight: 900;
          color: white;
          background-color: #97b27b;
          height: min-content;
          padding: 4px;
          position: relative;
          right: 15px;
          top:7px;
        }
    }
}
</style>