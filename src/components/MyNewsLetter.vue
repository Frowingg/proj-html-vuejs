<template>
  <section id="news-letter">
    <div class="container">
        <h2>Sign up to our Newsletter</h2>
        <input type="text">
        <button class="btn">SUBSCRIBE</button>
        <p>(we don't share your data with anybody, and only use it for it intended purpouse)</p>
    </div>
  </section>
</template>

<script>
export default {
    name: 'MyNewsLetter'
}
</script>

<style lang="scss" scoped>
.container{
    width: 30%;
    text-align: center;
    padding: 40px 0
}
#news-letter{
    background-image: url(../assets/img/newsletter_background.jpg);
    h2{
        margin-bottom: 40px
    }
    input{
        width: 100%
    }
    button{
        width: 100%;
        margin: 20px 0
    }
    p{
        font-size: 11px;
        font-weight: 300;
    }
}
</style>