<template>
  <div class="home">
  <header>
        <div class="title">Face Restoration &#174;</div>
        <div class="nav">
            <div class="navItem"><router-link to="/">Home</router-link></div>
            <div class="navItem">Paper</div>
            <div class="navItem">Contact</div>
        </div>
        <div class="contact">GitHub</div>
    </header>

    <div class="container">
        <div class="left">
            <div class="title"><text>Magic SR</text></div>
            <div class="slogan">Enhanced Face Restoration Guided by Multi-Exemplar Images</div>
            <div class="try">Try it now</div>
            <div class="imgType">Support for .jpge / .jpg / .png / .jiff / .webp</div>
        </div>
        <div class="right">
            <div class="blur"><img src="../assets/image/manyImages22.jpg" alt="album"></div>
            <div class="clear"><img src="../assets/image/manyImages2.jpg" alt="album"></div>
        </div>
    </div>
    <div class="next">﹀</div>
    <Uploader msg="Clear"/>
    <Uploader msg="Unclear"/>
  </div>
</template>

<script>
import Uploader from '@/components/Uploader.vue'

export default {
  name: 'Home',
  components: {
    Uploader
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}
/* header */
header{
    min-height: 16vh;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 2rem;
}
header .title{
    display: flex;
    align-items: center;
    font-weight: bold;
    width: 20rem;
}
.navItem{
    display: inline;
    margin: 0 4rem;
    line-height: 4rem;
    opacity: 0.4;
    box-sizing: content-box;
    transition: 0.2s linear;
    font-size: 1.5rem;
}
.navItem:hover{
    opacity: 1;
    border-bottom: 4px solid #8f94fb;
}
.contact{
    background-color: #000;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 16rem;
    margin-left: 4rem;
    height: 4rem;
    border-radius: 4rem;
    transition: letter-spacing 0.2s linear;
}
.contact:hover{
    letter-spacing: 2px;
}
/* footer */
footer{
    min-height: 16vh;
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0.5;
}
/* main */
.container{
    margin-top: 8vh;
    min-height: 52vh;
    padding: 2rem auto;
    display: flex;
    justify-content: space-between;
}
.container .left{
    width:28vw;
    display: flex;
    flex-direction: column;
    justify-content:space-around;
}
.container .left .title{
    font-size: 12rem;
    font-weight: bolder;
    animation: showTitle 1.6s linear forwards;
}
@keyframes showTitle {
    from{
        /* color: #8f94fb; */
        opacity: 0.2;
        letter-spacing: 4px;
        transform: scale(1.01);
    }
    to{
        color: #000;
        opacity: 1;
        letter-spacing: 0;
    }
}
.left .slogan{
    width: 24rem;
    font-size: 2rem;
}
.left .try{
    width: 12rem;
    height: 4rem;
    text-align: center;
    border: 3px solid #000;
    border-radius: 3rem;
    font-size: 1.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: 0.2s linear;
}
.left .imgType{
    opacity: 0.5;
}
.left .try:hover{
    background-color:#000;
    color:#fff;
}
.container .right{
  color: white;
  position: relative;
  width:40vw;
  overflow: hidden;
}
.blur , .clear{
  position: absolute;
}
.blur img{
  position: absolute;
  width: 40vw;
  animation-delay: 0.5s;
}
.clear{
    z-index: 1;
    animation: toShow 2s linear forwards;
    animation-delay: 1s;
}
.clear img{
  position: absolute;
  width: 40vw;
  z-index: 1;
}
@keyframes toShow {
    from {
        transform: translateX(100%);
    }
    to {
        transform: translateX(0%);
    }
}

.next{
    margin-top: 12vh;
    text-align: center;
    color: #000;
    height: 18vh;
    font-size: 10rem;
    animation: toNext 2s linear infinite;
}
@keyframes toNext {
    0% {
        opacity: 0.2;
    }
    40% {
        opacity: 1;
        transform: translateY(2vh);
    }
    80% {
        opacity: 0.4;
        transform: translateY(4vh);
    }
    90%{
        opacity: 0;
        transform: translateY(4vh);
    }
    100%{
        opacity: 0;
        transform: translateY(4vh);
    }
}
</style>