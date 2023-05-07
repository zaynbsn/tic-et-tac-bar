<template>
    <div class="bg-yellow">
         <div class="container">
            <div class="d-flex justify-content-center">
                <div class="p-5 text-center textCarreJaune">
                    <h3 class="text-white">Du lundi au samedi de 16h30 à 00h30</h3>
                </div>
            </div>
         </div>
    </div>
    <div class="bg-other ">
        <div class="container pt-3 myContainerToEnlarge">
            <div class="row text-white text-center mt-6 pt-3 myContainerToEnlarge">
                <div class="col-sm">
                    <h3 class="text-yellow mt-3">Adresse</h3>
                        <a class="text-white text-decoration-none text-yellow" target="_blank" href="https://goo.gl/maps/cFoXf1NKT4SvT6Fn8">
                            <p>135 Rue Sébastien Gryphe</p>
                        </a>
                    <p>69007 LYON</p>
                </div>
                <div class="col-sm">
                    <h3 class="text-yellow">Contact</h3>
                    <address>
                        <p class="text-break"><a class="text-white ms-2 text-decoration-none text-yellow" href="mailto:contact@tic-et-tac-bar.fr">contact@tic-et-tac-bar.fr</a></p> 
                    </address>
                </div>
                <div class="col-sm">
                    <h3 class="text-yellow">Horaires</h3>
                    <p>Lundi - Samedi</p>
                    <p>16h30 à 00h30</p>
                </div>
                
            </div>
            <div class="container-fuiled">
                <!-- row -->
                <div class="row">
                    <!-- copyright column -->
                    <div class="col-sm">
                        <div class="pt-3 text-white text-center">
                            © {{date}} Copyright 
                            <p class="text-white text-decoration-none">Tic &amp; Tac Bar</p>
                        </div>
                    </div>
                    <!-- links column -->
                    <div class="col-sm text-white text-center fs-3">
                        <div class="row myIcons">
                            <div class="col-sm-6">
                                <!-- Instagram link -->
                                <a class="text-white text-decoration-none" href="https://www.instagram.com/tic.et.tac.bar/"><fa :icon="['fab','instagram']" class="text-yellow" /></a>
                                <!-- Google map link-->
                                <a class="text-white text-decoration-none mySiteIcons" href="https://goo.gl/maps/AMMvjQtaDPKYQYaSA"><fa :icon="['fas','map-location-dot']" class="text-yellow"/></a>
                                <!-- Mail link -->
                                <a class="text-white text-decoration-none mySiteIcons" href="mailto:tic.et.tac.bar@gmail.com"><fa :icon="['fas','envelope']" class="text-yellow"/></a>
                            </div>  
                        </div>
                    </div>
                    <!-- Privacy Policy link and Terms Condition link column -->
                    <div class="col-sm p-3  text-white text-center">
                        <div class="col">
                        <a href="javascript:void(0)" class="text-decoration-none text-white pe-3">Menu </a>
                        <a href="javascript:void(0)" class="text-decoration-none text-white ps-3"> Autre lien</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { ref } from 'vue'
    export default {
        name:'foot',
        setup(){
            //Copyright Date
            const date=ref(new Date().getFullYear())
            return{
                date
            }
        }
    }
</script>

<style scoped>
@font-face {
    font-family: "Noto Sans";
    src: local("Noto Sans"),
    url(@/assets/fonts/NotoSans-Regular.ttf) format("truetype");
}

.bg-other{
    background-color: #000
}

.bg-yellow{
    background-color: #f6a424
}

.text-yellow{
    color: #f6a424
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
    .textCarreJaune{
        width:100%!important
    }

    .showOnPC{
        display: none
    }

    .myContainerToEnlarge{
        width: 100%!important;
        margin: 0!important;
        padding: 0!important
    }

    .myIcons{
        display: inline-block!important;
        width: 100%!important
    }

    .mySiteIcons{
        margin-left: 10%!important;
    }
}

@media screen and (min-device-width: 720px) {
    .mySiteIcons{
        padding-left:25%!important
    }

    .myIcons{
        display: inline-block!important;
        width: 100%!important
    }
}
/* For Mobile Landscape View */
@media screen and (max-device-width: 640px)
and (orientation: landscape) {

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
