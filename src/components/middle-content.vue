<template>
    <div class="div__middle">

        <div class="div__middle__up">
            <div class="header">
                <div>
                    <a class="left-right"><em class="fas fa-chevron-left"></em></a>
                    <a class="left-right"><em class="fas fa-chevron-right"></em></a>
                </div>

                <div class="header__profil">
                    <a class="header__profil__a">
                        <img id="header__img" src="../assets/profil.jpg" width="24px" alt="Image de profil">
                    </a>

                    <a class="header__profil__a">Untel</a>

                    <a class="header__profil__a"><em class="fas fa-caret-down"></em></a>
                </div>
            </div>

            <!------->

            <div class="header__playlist">
                <img id="header__playlist__img" src="../assets/img_son_playlist.jpg" width="190px" alt="">

                <div class="header__playlist__details">
                    <a id="playlist_publique">Playlist publique</a>
                    <h3 id="salsa_cubana">Salsa cubana</h3>
                    <a id="lomejor">¡Lo mejor de la Salsa Cubana! Cover: Cela Cruz</a>
                    <br>
                    <a>
                        <img src="../assets/spotify.png" width="28px" alt="">
                        <span class="details__span">Spotify</span>
                        <span class="details__span"><em class="fas fa-circle"></em> 180 478 likes</span>
                        <span class="details__span"><em class="fas fa-circle"></em> 48 titres,</span>
                        <span id="lomejor"> 4h</span>
                    </a>
                </div>
            </div>
        </div>
        <!----->
        <div class="div__middle__down">
            <div>
                <a><em class="fa-solid fa-play div__middle__down__icon"></em></a>
                <a><em class="fa-solid fa-heart div__middle__down__icon"></em></a>
                <a><em class="fa-solid fa-solid fa-arrow-down div__middle__down__icon"></em></a>
                <a><em class="fas fa-ellipsis-h div__middle__down__icon"></em></a>
            </div>

            <div class="div__middle__search_and_tri">
                <a><em class="fas fa-search"></em></a>
                <a>Tri personnalisé <em class="fas fa-caret-down"></em></a>
            </div>


            <div class="tableau">
                <div class="row">
                    <div class="col col__content__num">
                        <h1 class="col__titre">#</h1>
                    </div>
                    <div class="col col__content__titre">
                        <h1 class="col__titre">Titre</h1>
                    </div>
                    <div class="col col__content__album">
                        <h1 class="col__titre">Album</h1>
                    </div>
                    <div class="col col__content__add">
                        <h1 class="col__titre">Ajouté le</h1>
                    </div>
                    <div class="col col__content__clock">
                        <h1 class="col__titre"><em class="far fa-clock"></em></h1>
                    </div>
                </div>

                <div id="hr"></div>

                <div class="row row__liste">
                    <div class="col col__content__num">
                        <h1 class="col__titre__list">1</h1>
                    </div>
                    <div class="col col__content__titre">
                        <h1 class="col__titre__list col__titre_auteur">
                            <img src="../assets/profil.jpg" width="40px" alt="">
                            <div id="img_space_titre">
                                <a id="titre">Lorem ipsum</a>
                                <br>
                                <a>Lorem ipsam</a>
                            </div>
                        </h1>
                    </div>
                    <div class="col col__content__album">
                        <h1 class="col__titre__list">Lorem ipsum</h1>
                    </div>
                    <div class="col col__content__add">
                        <h1 class="col__titre__list">25 août 2020</h1>
                    </div>
                    <div class="col col__content__clock">
                        <h1 class="col__titre__list">3:05</h1>
                    </div>
                </div>
                
            </div>
        </div>
           
    </div>
</template>

<script>
export default {
    name: 'MiddleContent'
}
</script>

<style scoped>
.div__middle{
    float:right;
    width:1296px;
    height: 640px;
}
.div__middle__up{
    width:1296px;
    height: 290px;
    background: linear-gradient(to bottom, #F0692A, #AA491C);
    padding-top:8px;
    padding-left:20px;
}
.header{
    display:flex;
    justify-content: space-between;
}
.left-right{
    padding:10px;
    border-radius: 100%;
}
.fa-chevron-left{
    color:white;
    background-color: #191414;
    padding: 9px;
    padding-left:12px;
    padding-right: 12px;
    border-radius: 100%;
    font-size: 18px;
}
.fa-chevron-right{
    color:white;
    background-color: #191414;
    padding: 9px;
    padding-left:12px;
    padding-right: 12px;
    border-radius: 100%;
    font-size: 18px;
}
.header__profil{
    margin-top:3.5px;
    width:110px;
    height:30px;
    background-color:#191414;
    margin-right: 2.5%;
    border-radius: 100px;

    display: flex;
    justify-content: space-around;
    padding-left:5px;
    padding-right:10px;
    padding-top:2.5px;
}
.header__profil__a{
    color: #fbfbfb !important;
}
.fa-caret-down{
    margin-left:7px;
}
#header__img{
    border-radius: 100%;
    margin-top:-2px;
    margin-left:-7px;
}
/***/
.header__playlist{
    padding-top:30px;
    padding-left:11px;
}
#header__playlist__img{
    filter: drop-shadow(0 0 0.60rem #1E1E1E);
}
.header__playlist__details{
    margin-left:19%;
    margin-top:-190px;
}
#playlist_publique{
    text-transform: uppercase;
    color:white;
    font-weight: bold;
    letter-spacing: 0.7px;
}
#salsa_cubana{
    color:white;
    font-weight: bold;
    font-size: 80px;
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif
}
#lomejor{
    color: #BCBDBE;
    /* font-weight: bold; */
    letter-spacing: 0.7px;
    font-size: 15px;
}
.details__span{
    padding-left:3px;
    padding-right: 3px;
    color: white;
    font-weight: bold;
    letter-spacing: 0.7px;
    font-size: 15px;
    padding-top:10px;
}
.fa-circle{
    font-size: 5px;
    padding-right: 2px;
}
/********/
.div__middle__down{
    padding-left:30px;
    padding-top:15px;
    width:1296px;
    height: 410px;
    background:linear-gradient(to bottom, #8E3C16 5%, #191414 95%)
}
.div__middle__down__icon{
    padding:12px;
    float:left;
}
.fa-play{
    font-size:22px;
    color:#191414;
    background-color:#1DB954;
    border-radius: 100%;
    padding-top:16px;
    padding-bottom:16px;
    padding-right:16px;
    padding-left:21px;
}
.fa-heart{
    font-size:30px;
    color:#1DB954;
    margin-left:14px;
}
.fa-arrow-down{
    font-size:22px;
    color: #BCBDBE;
}
.fa-ellipsis-h{
    font-size:24px;
    color:white;
}
/***/
.div__middle__search_and_tri{
    padding-top:10px;
    display:flex;
    justify-content:space-between;
    color:#BCBDBE;
    /* font-weight: bold; */
    float:right;
    width: 170px;
    height:500px;
    margin-right:3.5%;
}
/***/
.tableau{
    margin-top:80px;
}
.col__titre{
    font-size:14px;
    color:#BCBDBE;
    text-transform: uppercase;
}
.col__content__num{
    margin-right: -200px;
}
.col__content__titre{
    padding-right: 220px;
}
.col__content__album{
    padding-right: 120px;
}
.col__content__add{
    padding-right: 120px;
}
.col__content__clock{
    margin-right: -375px;
}
#hr{
    height:1px;
    width:80%;
    position:absolute;
    background-color:#BCBDBE;
    margin-top:5px;
}
/***/
.row__liste{
    margin-top:30px;
}
.col__titre__list{
    font-size:16px;
    color:#BCBDBE;
}
.col__titre_auteur{
    display:flex;
    justify-content:center;
    margin-top:-10px;
    margin-left:-67px;
}
#img_space_titre{
    margin-left:10px;
}
#titre{
    font-size:19px;
    color:white;
    letter-spacing:0.5px;
}
</style>