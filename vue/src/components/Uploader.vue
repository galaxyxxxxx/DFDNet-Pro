<template>
    <div id="use">
        <div class="head">
            <div class="left">
                <div class="add">+</div>
                <div class="title">Upload Some Clear Images /</div>
            </div>
            <div class="right">
                Clear All
            </div>
        </div>
        
        <div class="main">
                <div class="upload">
                    <div class="top">
                        <div class="dragImg"><img src="../assets/image/image.png" alt="" srcset=""></div>
                        <div class="dragTitle">Drag & drop <span style='color:#8f94fb'>images</span> which are <span style='color:#8f94fb'>clear</span></div>
                        <div class="dragTip">or <span style='color:#8f94fb; border-bottom: 2px solid #8f94fb;'>browse file</span> on your computer</div>
                    </div>
                    <div class="uploadImg">image folder</div>
                    <div class="uploadBtn">Upload</div>
                </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            imageFolder: []
        }
    },
    props: {
        msg: {
            type: String,
            default: ''
        }
    }
}
</script>

<style scoped>
#use .main{
    /* background-color: #ffffff80; */
    border-radius: 4rem;
    min-height: 50vh;
    padding: 2rem 0;
    
    display: flex;
    flex-direction: column;
    justify-content:space-between;
    align-items:center;
}
.head{
    min-height: 4vh;
    display:flex;
    justify-content: space-between;
    align-items:center;
    margin: 2rem 0;
    font-size: 2rem;
}
.head .left{
    display:flex;
    align-items:center;
}
.add{
    border: 4px solid #000;
    border-radius: 2rem;
    font-weight: bolder;
    font-size: 2rem;
    height: 2rem;
    width: 2rem;
    display: flex;
    justify-content:center;
    align-items:center;
}
.head .left .title{
    margin-left: 1rem;
}
.head .right{
    border-bottom: 2px solid #00000080;
}
.process{
    display: flex;
    justify-content: center;
}
.processItem{
    color: #00000080;
    margin-left: 4rem;
}
.upload{
    background-color: #fff;
    border-radius: 2rem;
    box-shadow: -1rem 1rem 2rem #8f94fb80;
    display: flex;
    flex-direction: column;
    justify-content:space-around;
    align-items:center;
    min-height: 40vh;
}
.top{
    margin: 4rem;
    
    border: 4px dashed #8f94fb80;
    border-radius: 2rem;
    width: 40vw;
    height: 20vh;
    display: flex;
    flex-direction: column;
    justify-content:space-around;
    align-items:center;
    padding: 2rem 0 ;
}
.dragImg img{
    flex: 1;
    max-height: 8vh;
    animation: toSwag 1s linear alternate infinite;
}
@keyframes toSwag {
    0% {
        opacity: 0.8;
        transform: rotate(-15deg);
    }
    50%{
        opacity: 1;
        transform: rotate(0deg);
    }
    100% {
        opacity: 0.8;
        transform: rotate(15deg);
    }
}
.dragTitle{
    width: 24rem;
    font-size: 2rem;
    font-weight: bold;
    text-align: center;
}

.uploadBtn{
    color: #fff;
    background-color: #8f94fb;
    display: flex;
    justify-content: center;
    align-items:center;
    width: 12rem;
    height: 4rem;
    font-size: 1.5rem;
    border-radius: 2rem;
}
</style>