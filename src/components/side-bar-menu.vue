<template>
    <div class="div__sidebar">
        <div class="div__sidebar___menu">
            <a id="icon__sidebar__ellipsis"><em class="fas fa-ellipsis-h"></em></a>

            <ul>
                <li><em class="fas fa-home icon__sidebar__menu"></em> Accueil</li>
                <li><em class="fas fa-search icon__sidebar__menu"></em> Rechercher</li>
                <li><em class="fas fa-signal icon__sidebar__menu"></em> Bibliothèque</li>

                <br>

                <li><em class="fas fa-plus-square icon__sidebar__menu"></em> Créer une playlist</li>
                <li><em class="fas fa-heart icon__sidebar__menu"></em> Titres likés</li>
                <li><em class="fas fa-bookmark icon__sidebar__menu"></em> Vos épisodes</li>
            </ul>

            <hr id="hr__sidebar__menu">
        </div>
        <!----->
        <div class="div__sidebar__playlist">
            <ul>
                <li>Playlist n°1</li>
                <li class="playlist__active">Salsa cubana</li>
            </ul>

            <img alt="Logo playlsit" id="div__sidebar__logo__playlist" src="../assets/historia_de_un_amor.jpg" />
        </div>
        <!----->
        
    </div>
</template>

<script>
export default {
    name: 'SideBarMenu'
}
</script>

<style scoped>
.div__sidebar{
    width:240px;
    height: 630px;
    background-color:#191414;
}
.div__sidebar___menu{
    padding-top:5px;
    color:white !important;
}
#icon__sidebar__ellipsis{
    margin-left:33px;
    font-size:21px;
}
li{
    list-style-type: none !important;
    text-decoration:none !important;
    padding-top:6px;
    padding-bottom: 6px;
    color: #BCBDBE;
    font-weight:500;
    letter-spacing:0.8px;
    font-size:15px;
}
.icon__sidebar__menu{
    margin-right: 13px;
    font-size:17px;
}
.fa-bookmark{
    color:#1DB954;
}
#hr__sidebar__menu{
    color:#fbfbfb;
    margin-left:33px;
    margin-right:20px;
}
/**************/
.div__sidebar__playlist{
    width:100%;
    height:190px;
}
.playlist__active{
    color: white;
}
#div__sidebar__logo__playlist{
    width:100%;
}
</style>