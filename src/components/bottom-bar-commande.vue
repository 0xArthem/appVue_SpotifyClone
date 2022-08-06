<template>
    <div class="div__bottombar">
        <div class="div__bottombar__left">
            <a id="div__bottombar__left__heart">
                <em class="far fa-heart"></em>
            </a>

            <h3 id="div__bottombar__left__titre_musique">Historia de un Amor</h3>
            <p id="div__bottombar__left__auteur_musique">
                <span>Leo Marini</span>,
                <span>La Sonora Matancera</span>
            </p>
        </div>
        <!------>
        <div class="div__bottombar__middle">

            <div class="div__bottombar__middle__up">
                <a class="div__bottombar__middle__up__icon"><em class="fas fa-random"></em></a>
                <a class="div__bottombar__middle__up__icon"><em class="fas fa-step-backward"></em></a>
                <a class="div__bottombar__middle__up__icon"><em class="fas fa-play-circle"></em></a>
                <a class="div__bottombar__middle__up__icon"><em class="fas fa-step-forward"></em></a>
                <a class="div__bottombar__middle__up__icon"><em class="fas fa-redo"></em></a>
            </div>
            <!---->
            <div class="div__bottombar__middle__down">
                <a class="minute_song">0:00</a>
                <div id="load_song"></div>
                <a class="minute_song">2:49</a>
            </div>

        </div>

        <div class="div__bottombar__right">

            <a><em class="fas fa-microphone div__bottombar__right__icon"></em></a>
            <a><em class="fas fa-bars div__bottombar__right__icon"></em></a>
            <a><em class="fab fa-bluetooth-b div__bottombar__right__icon"></em></a>
            <a><em class="fas fa-volume-down div__bottombar__right__icon"></em></a>
            <div id="load_volume"></div>
            <a><em class="fas fa-arrows-alt-v div__bottombar__right__icon"></em></a>

        </div>
    </div>
</template>

<script>
export default {
    name: 'BottomBarCommande'
}
</script>

<style scoped>
.div__bottombar{
    /* border-top:solid 0.1px #BCBDBE; */
    position: absolute;
    margin-top: 10px;
    width:100%;
    height:80px;
    background-color: #191414;
    display:flex !important;
    justify-content: space-between !important;
}
.div__bottombar__left{
    width:240px;
    height:100%;
    padding-left:12px;
    padding-top:18px;
    /* float:left; */
}
#div__bottombar__left__titre_musique{
    color: white;
    font-size: 14.5px;
    font-weight: bold;
    letter-spacing: 0.6px;
}
#div__bottombar__left__auteur_musique{
    margin-top: -7px;
    color: #BCBDBE;
    font-size: 13px;
}
#div__bottombar__left__heart{
    float:right;
    padding-right:13px;
    margin-top:7px;
    color:#BCBDBE;
}
/********/
.div__bottombar__middle{
    /* background-color:red; */
    width:560px;
    height:100%;
}
.div__bottombar__middle__up{
    margin-top:-13px;
    display: flex;
    justify-content:center;
    padding:15px;
}
.div__bottombar__middle__up__icon{
    padding:17px;
    color: #ADA9A9;
}
.fa-redo{
    color: #1DB954;
    font-size: 15px;
}
.fa-random{font-size: 15px;}
.fa-step-backward{font-size: 21px;}
.fa-step-forward{font-size: 21px;}
.fa-play-circle{
    color:white;
    font-size: 33px;
    margin-top:-6px;
}
/**/
.div__bottombar__middle__down{
    margin-top:-20px;
    display: flex;
    justify-content: center;
}
.minute_song{
    margin-top:-8px;
    color: #ADA9A9;
    font-size:13px;
}
#load_song{
    width:100%;
    height:4px;
    background: #ADA9A9;
    border-radius: 4px;
    margin-left:10px;
    margin-right: 10px;
}
/********/
.div__bottombar__right{
    width:240px;
    height:100%;
    display:flex;
    justify-content: center;
    padding-top: 20px;
}
#load_volume{
    width: 75px;
    height: 4px;
    border-radius: 4px;
    background-color: white;
    margin-top:14px;
}
.div__bottombar__right__icon{
    color: #ADA9A9;
    padding: 8px;
    font-size:17px;
}
.fa-arrows-alt-v{
    transform: rotate(30deg);
    margin-left:6px;
}
</style>