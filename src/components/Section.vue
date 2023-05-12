<template >
    <div class="bg-black">
        <svg class="svg-down" width="192" height="61" version="1.1" xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" viewBox="0 0 160.7 61.5" enable-background="new 0 0 160.7 61.5" xml:space="preserve"><path fill="#000" d="M80.3,61.5c0,0,22.1-2.7,43.1-5.4s41-5.4,36.6-5.4c-21.7,0-34.1-12.7-44.9-25.4S95.3,0,80.3,0c-15,0-24.1,12.7-34.9,25.4S22.3,50.8,0.6,50.8c-4.3,0-6.5,0,3.5,1.3S36.2,56.1,80.3,61.5z"></path></svg>
        <div class="arrow-down"></div>

        <div>
            <!-- Offer -->
            <Offer />

            <!-- Discover -->
            <Discover />

            <div class="container">
                <!-- Our Quality -->
                <div class="row pt-5 pb-5">
                    <div class="col-sm-7 mb-4 mb-lg-0 ">
                        <div class="card cardInspi rounded-3 p-1 border-12  Computercard shadow">

                            <img class="card-img-top w-150" :src="inspiPic" alt="Card image" >

                            <div class="card-body rounded-bottom p-3 text-center cardInspi pt-1">
                                <h5 class="card-title text-warning fw-bold mt-3 myh5">Nous concernant</h5>

                                <p class="card-text text-white text-justify fs-6 textJustify">Le projet du bar Tic & Tac est né au détour d’une discussion en 2018. Il est le fruit de notre rencontre, Théo et Carl, sur les bancs de la fac. Littéralement indissociables, tout le monde nous appelait « Tic & Tac ». Nous avons donc naturellement choisi par la suite de nommer notre bar ainsi. Initialement prévu à Valence en Espagne, c’est bien à Lyon que nous avons finalement décidé d’ouvrir notre premier bar. Nous avons mis dans ce dernier les ingrédients résultant de tous les moments que nous avons partagés à deux comme nos nombreux voyages. C’est un bar à notre image, à celle de Tic & Tac.</p>
                            </div>
                        </div>
                    </div>

                    <div class="col-sm showOnPhone">
                        <router-link class="nav-link nav-logo nav-item " to="/About">
                            <h2 class="text-center fs-7 fw-bold p-3 yeltitle pt-3 pb-3 myH2"><ins>En savoir plus</ins></h2>
                        </router-link>   
                    </div>
                </div>
            </div>
        <!-- Our Quality -->
        </div>
    </div>
    <!-- Our Products -->
    <div  class="bg-dark h-small text-center">
        <div class="container p-2">
            <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
                <div class="carousel-inner">
                    <div class="carousel-item active p-3">
                        <div class="row row-cols-1 row-cols-md-3 g-4 showOnPC">
                            <div class="col cardCarrou">
                                <div class="card cardCarrou">
                                <img :src="Cocktail1"  class="card-img-top" alt="...">
                                
                                </div>
                            </div>
                            <div class="col cardCarrou">
                                <div class="card cardCarrou">
                                <img :src="Cocktail2"  class="card-img-top" alt="...">
                                
                                </div>
                            </div>
                            <div class="col cardCarrou">
                                <div class="card cardCarrou">
                                <img :src="Cocktail4"  class="card-img-top" alt="...">
                                
                                </div>
                            </div>
                            <div class="col cardCarrou">
                                <div class="card cardCarrou">
                                <img :src="Cocktail5"  class="card-img-top" alt="...">
                                
                                </div>
                            </div>
                            <div class="col cardCarrou">
                                <div class="card cardCarrou">
                                <img :src="Cocktail6"  class="card-img-top" alt="...">
                                
                                </div>
                            </div>
                        </div>
                        <div class="row row-cols-1 row-cols-md-4 g-4 showOnPhone">
                            <div class="col cardCarrou">
                                <div class="row row-cols-1 row-cols-md-2">
                                    
                                    <div class="col cardCarrou2">
                                        <div class="card ">
                                        <img :src="Cocktail1"  class="card-img-top" alt="...">
                                        </div>
                                    </div>
                                    <div class="col cardCarrou2">
                                        <div class="card ">
                                        <img :src="Cocktail2"  class="card-img-top" alt="...">
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="col cardCarrou">
                                
                                <div class="row row-cols-1 row-cols-md-2">
                                    <div class="col cardCarrou2">
                                        <div class="card ">
                                        <img :src="Cocktail4"  class="card-img-top" alt="...">
                                        </div>
                                    </div>
                                    <div class="col cardCarrou2">
                                        <div class="card ">
                                        <img :src="Cocktail5"  class="card-img-top" alt="...">
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="carousel-item p-3">
                        <div class="row row-cols-1 row-cols-md-4 g-4 showOnPhone">
                            <div class="col cardCarrou">
                                <div class="row row-cols-1 row-cols-md-2">
                                    
                                    <div class="col cardCarrou2">
                                        <div class="card ">
                                        <img :src="Cocktail6"  class="card-img-top" alt="...">
                                        </div>
                                    </div>
                                    <div class="col cardCarrou2">
                                        <div class=" ">
                                        <img :src="CocktailNull"  class="card-img-top" alt="...">
                                        </div>
                                    </div>
                                </div>
                             </div>
                            <div class="col cardCarrou">
                                
                                <div class="row row-cols-1 row-cols-md-2">
                                    <div class="col cardCarrou2">
                                        <div class=" ">
                                        <img :src="CocktailNull"  class="card-img-top" alt="...">
                                        </div>
                                    </div>
                                    <div class="col cardCarrou2">
                                        <div class=" ">
                                        <img :src="CocktailNull"  class="card-img-top" alt="...">
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        
                    </div>
                </div>

                <button class="carousel-control-prev " type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
                    <span class="carousel-control-prev-icon" aria-hidden="false"></span>
                    <span class="visually-hidden">Précedent</span>
                </button>
                <button class="carousel-control-next " type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
                    <span class="carousel-control-next-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Suivant</span>
                </button>
            </div>
        </div>
    </div>
    <!-- Our Products -->
    <!-- Coffee Rates -->
    <div class="container-fluid bg-black pt-global">
        <div class="container">
            
            <div class="row  text-center pt-3">
                <div class="col-sm mb-4 text-white heightAvis">
                     <div class="shadow rounded1  p-5 mt-1 pt-2 pb-3 heightAvis text-white bg-dark">
                      <h2 class="bg-yellow rounded-circle p-4 badge  fs-4 text-white mb-4"><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /></h2>
                        <p class="text-secondary text-white">Bar super sympas avec des barmans au top, très accueillant. Des très bons cocktails et bières pour des prix tout à fait abordables. Je recommande l'adresse !!</p>
                        <hr>
                        <div class="row">
                            <div class="col"><p class="fw-bold text-white">Maxime M</p></div>
                        </div>
                    </div>
                </div>
                <div class="col-sm mb-4 text-white ">
                     <div class="shadow rounded1  p-5 mt-1 pt-2 pb-3 heightAvis text-white bg-dark">
                      <h2 class="bg-yellow rounded-circle p-4 badge  fs-4 text-white mb-4"><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /></h2>
                        <p class="text-secondary text-white">J’ai découvert ce bar par hasard et je peux que le conseiller !!
                            J’ai passé une super moment ! Et les cocktails sont excellents.</p>
                        <hr>
                        <div class="row">
                            <div class="col"><p class="fw-bold text-white">Robin B</p></div>
                        </div>
                    </div>
                </div>
                <div class="col-sm mb-4 text-white ">
                     <div class="shadow rounded1  p-5 mt-1 pt-2 pb-3 heightAvis text-white bg-dark">
                      <h2 class="bg-yellow rounded-circle p-4 badge  fs-4 text-white mb-4"><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /></h2>
                        <p class="text-secondary text-white">Des barmans passionnés, des cocktails uniques parfaitement dosés, hésitez pas</p>
                        <hr>
                        <div class="row">
                            <div class="col"><p class="fw-bold text-white">Matisse L</p></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Coffee Rates -->
<div class="container-fluid bg-black pt-global mapBar">
        <div class="container pb-3">
            <iframe class="h-100 w-100 rounded shadow" src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d11136.715939471307!2d4.8387141!3d45.7475576!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47f4eb7d9e819e2b%3A0xcf8fb327d3b9188a!2sTIC%20%26%20TAC%20BAR!5e0!3m2!1sen!2sfr!4v1682035826407!5m2!1sen!2sfr"    allowfullscreen="" loading="lazy"></iframe>
        </div>
</div>          
</template>

<script>
import { reactive, toRefs, ref } from 'vue'
import Offer from './Homepage/Offer.vue'
import Discover from './Homepage/Discover.vue'

export default {
    name:'Section',
    components: { Offer, Discover },
    setup(){
        let photos=reactive({
            inspiPic:require('@/assets/img/inspiration_picture.jpg'),
            Cocktail1:require('@/assets/img/Cocktail1.jpeg'),
            Cocktail2:require('@/assets/img/Cocktail2.jpeg'),
            Cocktail4:require('@/assets/img/Cocktail4.jpeg'),
            Cocktail5:require('@/assets/img/Cocktail5.jpeg'),
            Cocktail6:require('@/assets/img/Cocktail6.jpeg'),
            CocktailNull:require('@/assets/img/CocktailNull.jpeg'),
            fondcarousel:require('@/assets/img/cocktail-fond-plein.jpg'),
        })

        return {...toRefs(photos)}
    }
}
</script>

<style lang="scss" scoped>
@font-face {
    font-family: "Noto Sans";
    src: local("Noto Sans"),
    url(@/assets/fonts/NotoSans-Regular.ttf) format("truetype");
}
.mt-global{
    padding-top: 500px;
}

.yeltitle{
    color: #F6A424;  
    font-size:3.5em;
}

.yeltitlelower{
    color: #F6A424;  
    font-size:2.5em;
}
.rc{
    font-size: 100px;
    color: #F6A424;  
}
.yellow-hover:hover{
    background-color:#F6A424 ;
    color: #fff;
}
//color: #161228;
.dark-hover:hover{
    background-color: #fff;
    color: #F6A424;
}

.smPhone{
    justify-content:center;
}
.text-2A{
    color: #0000;
}
.bg-yellow{
    background: #F6A424;
}
.text-yellow{
    color: #F6A424;
}
.Computercard{
    width: 60%;
    margin-left:19%;
    background-color: black;
    border-color : #F6A424;
    text-align: justify;
    text-justify: inter-word;
    
}
.card{
    border: solid 3px #F6A424!important;
    border-color : #F6A424!important;}

// .textJustify{
//     text-align: justify;
//     text-justify: inter-word;
// }
ul li{
    text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}
.rounded1{
    border-radius: 30px;
}
.bg-other1{
    background-color: #fff;
}
.h-small{
    background-size: cover;
}
.card-title{
    color: #F6A424;
}

// .qualityParag{
//     text-align: justify;
// }


.svg-down {
    bottom: 8px;
    left: calc(50% - 96px);
    position: absolute;
    z-index: 5;
    margin-left: 0;
    margin-bottom: -3px;
    color: #fff;
}
.arrow-down{
    width: 48px;
    position: relative;
    height: 32px;
    left: 50%;
    bottom: 36px;
    transform: translate(-50%, 0);
    z-index: 10;
    background: url("../assets/icons/arrowDownWhite.svg") no-repeat center;
    background-size: contain;
}
.myCardsDiscover{
    margin:0 auto;
    padding:10px;
    padding-top:0px;
    height:200px;
}

.marginDiscoverCardTitle{
    margin-left:25%;
}
.paddingDiscoverCardTitle{
    padding-left:20%;
}

.heightAvis{
    height:300px;
}
.card-title{
    color : #F6A424!important;
}

.cardCarrou{
    height:100%;
    overflow: hidden;
    padding:2px;
}

.carousel-control-prev{
    height:100%;
}

.showOnPhone{
        display:none!important;
    }
/* For Desktop View */
@media screen and (min-width: 1024px) {

}

/* For Tablet View */
@media screen and (min-device-width: 768px)
and (max-device-width: 1024px) {

}

/* For Mobile Portrait View */
@media screen and (max-device-width: 480px)
and (orientation: portrait) {
    .myH2{
        font-size:1.7em;
        padding: 0px!important;
    }
    .showOnPC{
        display:none;
    }
    .myCardsDiscover{
        height:10%;
        margin-top:0!important;
        padding-top:5px!important;
        margin-bottom:5px!important;
        padding-bottom:5px!important;
        text-align: left!important;
        width:450px;
        text-align: left;
    }
    .paddingDiscoverCardTitle {
        padding-left:15px;
        text-align: left;
        color:white;
    }
    .marginDiscoverCardTitle{
        margin:0;
        text-align: left;
    }

    .smPhone{
        justify-content: start;
        text-align: left;
    }
    .textJustifyLeft{
        
        text-align: left;
    }

    .cardInspi{
        margin:0!important;
        width:100%;
    }
    .showOnPhone{
        display: block!important;;
    }
    
    .showOnPC{
        display:none;
    }

    .cardCarrou2{
        width:50%;
    }
    .myCardsDiscover{
        width:90%!important;
    }

    html{
        margin:0;
        padding:0;
        overflow: hidden;
    }
    .card-title{
        font-size:2em!important;
    }
}

/* For Mobile Landscape View */
@media screen and (max-device-width: 640px)
and (orientation: landscape) {

}
/* For PC */
@media screen and (min-device-width: 720px){

}
/* For Mobile Phones Portrait or Landscape View */
@media screen and (max-device-width: 640px) {
   
}

/* For iPhone 4 Portrait or Landscape View */
@media screen and (min-device-width: 320px)
and (-webkit-min-device-pixel-ratio: 2) {
}

/* For iPhone 5 Portrait or Landscape View */
@media (device-height: 568px) and (device-width: 320px)
and (-webkit-min-device-pixel-ratio: 2) {
}

/* For iPhone 6 and 6 plus Portrait or Landscape View */
@media (min-device-height: 667px) and (min-device-width: 375px)
and (-webkit-min-device-pixel-ratio: 3) {
}

</style>
