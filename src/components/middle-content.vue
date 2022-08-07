<template>
    <div class="div__middle" v-if="div__middle_playlist">

        <div class="div__middle__up">
            <div class="header">
                <div>
                    <a class="left-right" @click="goToAccueil()"><em class="fas fa-chevron-left"></em></a>
                    <a class="left-right"><em class="fas fa-chevron-right"></em></a>
                </div>

                <div class="header__profil" data-mdb-toggle="modal" data-mdb-target="#header__profil">
                    <a class="header__profil__a">
                        <img id="header__img" src="../assets/profil.jpg" width="24px" alt="Image de profil">
                    </a>

                    <a class="header__profil__a">Untel</a>

                    <a class="header__profil__a"><em class="fas fa-caret-down"></em></a>
                </div>
            </div>
            <!-- Modal -->
            <div class="modal fade" id="header__profil" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
                <div class="modal-dialog">
                    <div class="modal-body">
                        <ul>
                            <li>Compte</li>
                            <li>Profil</li>
                            <li>Session d'écoute privée</li>
                            <li>Préférences</li>
                            <hr>
                            <li>Deconnexion</li>
                        </ul>
                    </div>
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
                <a class="div__middle__search_and_tri__a"><em class="fas fa-search"></em></a>
                <a class="div__middle__search_and_tri__a">Tri personnalisé <em class="fas fa-caret-down"></em></a>
            </div>


            <div class="tableau">
            
                <div class="table-responsive"> 
                    <table class="table">
                        <thead class="thead">
                            <tr>
                                <th scope="col" class="col__titre">#</th>
                                <th scope="col" class="col__titre">Titre</th>
                                <th scope="col" class="col__titre">Album</th>
                                <th scope="col" class="col__titre">Ajouté le</th>
                                <th scope="col" class="col__titre">
                                    <em class="far fa-clock"></em>
                                </th>
                            </tr>

                            
                        </thead>

                        <!-------------->

                        <tbody>
                            <tr v-for="playlistMusic in playlistMusics" :key="playlistMusic.id">
                                <th scope="row">{{ playlistMusic.id }}</th>

                                <td class="text-light">
                                    <img
                                    v-bind:src="playlistMusic.url" alt="" style="width:50px;"
                                    >

                                    <div style="margin-top:-50px;margin-left:60px;">
                                        <a
                                        class="playSong__a"
                                        >{{ playlistMusic.title }}</a>
                                        <br>
                                        <a style="color:#ADA9A9;">{{ playlistMusic.author }}</a>
                                    </div>
                                    </td>
                                <td>{{ playlistMusic.album }}</td>
                                <td>{{ playlistMusic.add }}</td>
                                <td>{{ playlistMusic.time }}</td>
                            </tr>
                            <!----->
                        </tbody>
                    </table>
                </div>

            </div>
        </div>
    </div>
    <!--------------------------------------------->
    <div class="div__middle__accueil" v-if="div__middle_accueil">
    
        <div class="header__accueil">
            <div>
                <a class="left-right"><em class="fas fa-chevron-left"></em></a>
                <a class="left-right" @click="playlist()"><em class="fas fa-chevron-right"></em></a>
            </div>
        </div>

        <div class="header__banniere">
            <!---->
            <div style="float:left;">
                <img src="../assets/afro_hits.jpg" alt=""
                style="width:210px;margin-top:20px;margin-left:18px;">
            </div>

            <div style="margin-left:250px;padding-top:20px;color:white;">
                <a id="playlist_publique">Playlist</a>
                <h3 id="salsa_cubana">Afro Hits</h3>
                <a>Afropop feel good d'Europe et d'Afrique</a>
                <br>
                <button class="btn btn-rounded mt-3 btn__lecture">Lecture</button>
                <button class="btn btn-rounded btn__abonner">S'abonner</button>
            </div>
        </div>

        <h2 id="hello">Bonjour</h2>

        <div class="row row-cols-1 row-cols-md-3 g-3 row__accueil">
            
            <div class="col-sm-6">
                <img src="https://images.unsplash.com/photo-1588167056547-c183313da47c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=531&q=80"
                alt="" class="img__accueil__musique">
                <div class="card row__accueil__card">
                    <div class="card-body row__accueil__body">
                        
                        <h5 class="card-title row__accueil__title">Musique en cours #1</h5>
                        <div class="progress">
                            <div
                                class="progress-bar progress-bar-striped progress-bar-animated"
                                role="progressbar"
                                aria-valuenow="75"
                                aria-valuemin="0"
                                aria-valuemax="100"
                                style="width: 75%;"
                            ></div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col-sm-6">
                <img src="https://images.unsplash.com/photo-1531501410720-c8d437636169?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80"
                alt="" class="img__accueil__musique">

                <div class="card row__accueil__card">
                    <div class="card-body row__accueil__body">
                        <h5 class="card-title row__accueil__title">Musique en cours #2</h5>
                        <div class="progress">
                            <div
                                class="progress-bar progress-bar-striped progress-bar-animated"
                                role="progressbar"
                                aria-valuenow="75"
                                aria-valuemin="0"
                                aria-valuemax="100"
                                style="width: 95%;"
                            ></div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col-sm-6">
                <img src="https://images.unsplash.com/photo-1487537023671-8dce1a785863?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80"
                alt="" class="img__accueil__musique">
                <div class="card row__accueil__card">
                    <div class="card-body row__accueil__body">
                        <h5 class="card-title row__accueil__title">Musique en cours #3</h5>
                        <div class="progress">
                            <div
                                class="progress-bar progress-bar-striped progress-bar-animated"
                                role="progressbar"
                                aria-valuenow="75"
                                aria-valuemin="0"
                                aria-valuemax="100"
                                style="width: 45%;"
                            ></div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col-sm-6">
                <img src="https://images.unsplash.com/photo-1508700115892-45ecd05ae2ad?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=869&q=80"
                alt="" class="img__accueil__musique">
                <div class="card row__accueil__card">
                    <div class="card-body row__accueil__body">
                        <h5 class="card-title row__accueil__title">Musique en cours #4</h5>
                        <div class="progress">
                            <div
                                class="progress-bar progress-bar-striped progress-bar-animated"
                                role="progressbar"
                                aria-valuenow="75"
                                aria-valuemin="0"
                                aria-valuemax="100"
                                style="width: 15%;"
                            ></div>
                        </div>
                    </div>
                </div>
            </div>
            
        </div>

    </div>
</template>

<script>
export default {
    name: 'MiddleContent',
    data() {
        return {
            div__middle_playlist: true,
            div__middle_accueil: false,
            playlistMusics: [
                {
                    id:1,
                    title: "Vecina Présteme el Cubo",
                    author: "Pupy y Los Que Son Son",
                    album: "Tranquilo Que Yo Controlo (Remasterizado)",
                    add: "25 août 2020",
                    time: "3:05",
                    sound: "https://universal-soundbank.com/sounds/13748.mp3",
                    url: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8bWFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"
                },
                {
                    id:2,
                    title: "En la Selva",
                    author: "Maykel Blanco y Su Salsa Mayor, Pancho Amat",
                    album: "Que Tiene Que Te Mueve",
                    add: "25 août 2020",
                    time: "6:00",
                    sound: "https://universal-soundbank.com/sounds/13747.mp3",
                    url: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8bWFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"
                    
                },
                {
                    id:3,
                    title: "Me Dicen Cuba",
                    author: "Alexander Abreu, Havana D'Primera",
                    album: "La Vuelta al Mundo",
                    add: "25 août 2020",
                    time: "5:42",
                    sound: "https://universal-soundbank.com/sounds/13749.mp3",
                    url: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8bWFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"
                },
                {
                    id:4,
                    title: "Pa' Bravo Yo",
                    author: "Justo Betancourt",
                    album: "Pa' Bravo Yo",
                    add: "25 août 2020",
                    time: "3:45",
                    sound: "https://universal-soundbank.com/sounds/13746.mp3",
                    url: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8bWFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"
                },
                {
                    id:5,
                    title: "Soy Cubana",
                    author: "Son Damas",
                    album: "Bailables de Cuba, Vol.2",
                    add: "25 août 2020",
                    time: "5:09",
                    sound: "https://universal-soundbank.com/sounds/13639.mp3",
                    url: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8bWFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"
                },
                {
                    id:6,
                    title: "Historia de un Amor",
                    author: "Leo Marini, La Sonora Matancera",
                    album: "Latin Trumpets - Bolero",
                    add: "25 août 2020",
                    time: "2:49",
                    sound: "https://universal-soundbank.com/sounds/13821.mp3",
                    url: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8bWFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"
                
                },
                {
                    id:7,
                    title: "Hoah!",
                    author: "Calle Real",
                    album: "Dime Qué?!",
                    add: "25 août 2020",
                    time: "7:24",
                    sound: "https://universal-soundbank.com/sounds/20555.mp3",
                    url: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8bWFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"

                },
                {
                    id:8,
                    title: "Consumelo",
                    author: "TIMBALIVE",
                    album: "Consumelo",
                    add: "25 août 2020",
                    time: "4:42",
                    sound: "https://universal-soundbank.com/sounds/20815.mp3",
                    url: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8bWFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"

                },
                {
                    id:9,
                    title: "Yo Siempre LLamo La Fiesta",
                    author: "Marquetti, Habana Swing",
                    album: "Salsa 2018",
                    add: "25 août 2020",
                    time: "3:58",
                    sound: "https://universal-soundbank.com/sounds/13826.mp3",
                    url: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8bWFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"

                },
                {
                    id:10,
                    title: "Castigo",
                    author: "Leslie Guzman, Los Yakuza",
                    album: "Castigo",
                    add: "25 août 2020",
                    time: "3:36",
                    sound: "https://universal-soundbank.com/sounds/13819.mp3",
                    url: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8bWFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"

                }
            ]
        }
    },
    methods: {
        goToAccueil() {
            this.div__middle_playlist = false
            this.div__middle_accueil = true
        },
        playlist() {
            this.div__middle_playlist = true
            this.div__middle_accueil = false
        }
    }
}
</script>

<style scoped>
.div__middle{
    float:right;
    width:1296px;
    height: 640px;
    overflow-y: scroll;
    overflow-x: hidden;
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
.left-right:hover{
    cursor:pointer;
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
.header__profil:hover{
    cursor: pointer;
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
    /* height:100%; */
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
.div__middle__search_and_tri__a{color: #ADA9A9;transition-duration: 0.3s;}
.div__middle__search_and_tri__a:hover{
    color: white;
    transition-duration: 0.3s;
    cursor:pointer;
}
/***/
.tableau{
    margin-top:80px;
}
.col__titre{
    font-size:15px;
    color:#BCBDBE;
    text-transform: uppercase;
}
/***/
#img_space_titre{
    margin-left:10px;
}
#titre{
    font-size:17px;
    color:white;
    letter-spacing:0.5px;
}
/*****************************/
th{
    color:#ADA9A9;
    font-size:16px;
    border:none !important;
}
td{
    color:#ADA9A9;
    font-size:16px;
    border:none !important;
}
thead{
    border-bottom:solid 0.2px #ADA9A9;
}
/***/
.fa-ellipsis-h:hover{color:white;}
.fa-arrow-down:hover{color:white;}
.fa-heart:hover{color:#2AE86D;}
.fa-play:hover{
    padding-top:17px;
    padding-bottom:17px;
    padding-right:17px;
    padding-left:22px;
}
/*****/
.modal-dialog{
    background-color:#191414;
    margin-right:35px;
    margin-top:50px;
    width:200px;
}
ul{
    list-style-type: none;
    margin-left:-30px;
}
li{
    color:white;
    margin-top:10px;
    font-size:15px;
}
/*** */
.playSong__a{
    cursor:pointer;
    color:white;
}
/********************************************************************* */
.div__middle__accueil{
    background-color:#191414;
    float:right;
    float:right;
    width:1296px;
    height: 640px;
    overflow-y: hidden;
    overflow-x: hidden;
}
.header__accueil{
    padding-top:8px;
    padding-left:20px;
}
.header__banniere{
    height:250px;
    background-color:black;
    margin-left:3%;
    margin-right:3%;
    margin-top:1%;
    border-radius:8px;
}
#hello{
    margin-left:3%;
    margin-top:2%;
    margin-bottom:2%;
    color:#fbfbfb;
    font-weight: bold;
    letter-spacing:0.5px;
}
.row__accueil{
    margin-left:2.5%;
    margin-right:3%;
}
.row__accueil__card{
    border-radius:5px !important;
    margin-right:2%;
    margin-bottom:1%;
}
.row__accueil__body{
    background-color:#262626;
    color:#fbfbfb;
    text-transform: uppercase;
    letter-spacing:0.7px;
    transition-duration:0.8s;
}
.row__accueil__body:hover{
    background-color:#666262;
    cursor:pointer;
    transition-duration:0.8s;
}
.row__accueil__title{
    margin-left:-10px;
    font-size:15px;
    font-weight:bold !important;
}
.progress{
    margin-left:-10px;
    margin-right:70%;
    background-color:#ADA9A9;
    border-radius:10px;
    height:6px;
}
.progress-bar{
    border:solid 4px #fbfbfb;
    margin-left:-5px;
    border-radius:10px;
}
.img__accueil__musique{
    width:88px;
    height:80px;
    float:left;
}
.btn__abonner{
    letter-spacing:0.9px;
    margin-left:140px;
    margin-top:15px;
    color:white;
    background-color:black;
    font-weight:bold;
    font-size:16px;
    text-transform: none;
    border:solid 1px white;
    position:absolute;
}
.btn__abonner:hover{
    font-size:17px;
}
.btn__lecture{
    position:absolute;
    letter-spacing:0.9px;
    color:black;
    background-color:#1DB954;
    font-weight:bold;
    font-size:16px;
    text-transform: none;
    border:solid 1px #1DB954;
}
.btn__lecture:hover{
    font-size:17px;
}
</style>