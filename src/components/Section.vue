<template >
    <div class="bg-black">
        <svg class="svg-down" width="192" height="61" version="1.1" xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" viewBox="0 0 160.7 61.5" enable-background="new 0 0 160.7 61.5" xml:space="preserve"><path fill="#000" d="M80.3,61.5c0,0,22.1-2.7,43.1-5.4s41-5.4,36.6-5.4c-21.7,0-34.1-12.7-44.9-25.4S95.3,0,80.3,0c-15,0-24.1,12.7-34.9,25.4S22.3,50.8,0.6,50.8c-4.3,0-6.5,0,3.5,1.3S36.2,56.1,80.3,61.5z"></path></svg>
        <div class="arrow-down"></div>

        <div>
            <!-- Offer -->
            <Offer />

            <!-- Discover -->
            <Discover />

            <!-- About -->
            <About />

            <!-- Cocktails -->
            <Cocktails />

        <!-- Our Quality -->
        </div>
    </div>

    <!-- Coffee Rates -->
    <div class="container-fluid bg-black pt-global">
        <div class="container">
            
            <div class="row  text-center pt-3">
                <div class="col-sm mb-4 text-white heightAvis">
                     <div class="shadow rounded1  p-5 mt-1 pt-2 pb-3 heightAvis text-white bg-dark">
                      <h2 class="bg-yellow rounded-circle p-4 badge  fs-4 text-white mb-4"><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /><fa :icon="['fas','star']" class="" /></h2>
                        <p class="text-secondary text-white">Bar super sympas avec des barmans au top, très accueillant. Des très bons cocktails et bières pour des prix tout à fait abordables.</p>
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
import About from './Homepage/About.vue'
import Cocktails from './Homepage/Cocktails.vue'

export default {
    name:'Section',
    components: { Offer, Discover, About, Cocktails },
    setup(){
        let photos=reactive({
            inspiPic:require('@/assets/img/inspiration_picture.jpg'),
            Cocktail1:require('@/assets/img/cocktail1.png'),
            Cocktail2:require('@/assets/img/cocktail2.png'),
            Cocktail3:require('@/assets/img/cocktail3.png'),
            Cocktail4:require('@/assets/img/cocktail4.png'),
            Cocktail5:require('@/assets/img/cocktail5.png'),
            Cocktail6:require('@/assets/img/cocktail6.png'),
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
// .card{
//     border: solid 3px #F6A424!important;
//     border-color : #F6A424!important;
// }

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
