<template>
<!-- header background image -->
  <div :style="isTouch ? `backgroundImage: url(${barmobile})` : `backgroundImage: url(${bar})`" class="demo container-fluid" style="height: calc(100vh - 16px);">
    <div class="d-flex justify-content-center align-items-center" style="height: 100%">
      <!-- header text -->
        <div class="col-sm-12 d-flex flex-column justify-content-center align-items-center" id="blocDescription">
          <img :src="logonomono" class="myMonoLogo" id="logonomono" alt="tic&tac logo">

          <div class="row my-2">
            <div class="col text-center myText2">
              <h2>
                <span class="horairesAdresses horairesAdresses2 fs-5" data-v-3695d485="">135 Rue Sébastien Gryphe, 69007 LYON</span>
              </h2>
            </div>
          </div>
          
          <div class="row my-2">
            <div class="col text-center myText">
              <h3>
                <span class="horairesAdresses fs-3" style="color: #ff8000;">16h30 à 00h30</span>
                <br>
                <span class="semaine fs-3">Du lundi au samedi</span>
              </h3>
            </div>          
          </div>

          <div class="row my-2">
            <Button to="https://tic-et-tac-bar.fr/carte.pdf" label="Notre carte" blank />
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import { reactive,ref, toRefs } from 'vue'
import windowWidthMixin from '@/mixins/windowWidthMixin'
import Button from './UI/Button.vue'

    export default {
        name:'Homehead',
        components: { Button },
        mixins: [windowWidthMixin],
        setup(){
            let barEtVerre;
            //Button default class
            const githubstarover=ref('myButtonMenu btn btn-transparent  fs-7 border border-2 btn-hover  py-2 px-4 menuButton');
            //Button mouseover class
            const mouseover='myButtonMenu btn btn-transparent  fs-7 border border-2 btn-hover  py-2 px-4 menuButton textWhite';
            //Button mouseleave class
            const mouseleave='myButtonMenu btn btn-transparent  fs-7 border border-2 btn-hover  py-2 px-4 menuButton';
                try{
                //Check availability
                    barEtVerre=reactive({
                      bar:require('@/assets/img/header-img.jpg'),
                      barmobile:require('@/assets/img/header-mobile.jpg'),
                      monogram:require('@/assets/img/monogram.png'),
                      logonomono:require('@/assets/img/logo-navbar.png')
                    });
                }
                catch(error){
                console.error(error);
                }
            
                return{
                ...toRefs(barEtVerre),
                githubstarover,
                mouseover,
                mouseleave
                }
        }
    }
</script>

<style lang="scss" scoped>
@font-face {
    font-family: "Noto Sans";
    src: local("Noto Sans"),
    url(@/assets/fonts/NotoSans-Regular.ttf) format("truetype");
}
.demo{
  background-size: cover;
  background:#000;
  background-repeat: no-repeat;
  background-size: 100%;
}

.main-button{
  width: fit-content;
  height: fit-content;
  background-color: #fff;
  border-radius: 8px;
  padding: 0.6rem 1.2rem;
  text-decoration: none;
  color: black;
  font-size: 1rem;
  letter-spacing: 0.05em;
}
.menuButton{
  font-size: 50px;
  margin-left:5%;
  color: #F6A424; 
  border-color: #F6A424;
}
.letter{
  letter-spacing: 5px;
}
.btn-hover:hover{
  background-color: #F6A424; 
}

.pointer{
  cursor: pointer;
  margin-top: 20%;
}
.pointer:hover{
 animation-name: caffee-image;
 animation-duration: 4s;
 animation-iteration-count: infinite;
}
@keyframes caffee-image {
  0%   {margin-top:20%;}
  25%  {margin-top:17%;}
  50%  {margin-top:23%;}
  75%  {margin-top:17%;}
  100% {margin-top:20%;}
}
.text-yellow{
  color: #F6A424;
}

#logonomono{
  margin:0;
  padding:0;
  width:30%;
  display: inline-block;
}

#description{
  margin-left:5%;
  margin-top:5%;
  font-size:12em;
}

#blocDescription{
  margin-top:5%;
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
  .showOnPhone {
        display:block!important
    }

    .showOnPC {
        display: none!important
    }

    #logonomono,.myMonoLogo {
        width: 80%;
    }

    #blocDescription {
        background: rgba(0,0,0,0.6);
        padding: 1rem 0.5rem;
        border-radius: 16px;
    }

    .demo {
        background-size: cover;
        background-position: center;
    }

    .myButtonMenu {
        display: block;
        margin-left: auto;
        margin-right: auto
    }

    .test {
        margin-top: 20px
    }

    .horairesAdresses {
        font-size: 1.25em
    }

    .myText2 {
        width: 300px;
        font-size: 1.5em
    }

    .myRow2 {
        width: 100%!important
    }

    .myIcon {
        width: 50px;
        margin-top: 16px;
        font-size: 1.3em
    }

    .myText {
        width: 250px;
        color: #fff
    }

    .myRow {
        width: 100%!important;
        margin: 0!important;
        padding: 0!important;
        margin-left:.6em!important;
    }

    .myText2 {
        width: 250px;
        color: #fff
    }

    .myRow2 {
        width: 500px!important;
        margin: 0!important;
        padding: 0!important
    }

    .myIcon2 {
        font-size: 2em
    }

    .myDiv2 {
        width: 50px;
        margin-top: 16px;
        color: #fff
    }

    .horairesAdresses2 {
        font-size: .9em!important
    }
}

@media screen and (min-device-width: 720px) {
    .myText {
        color:#fff;
        width: 45%
    }

    .myIcon {
        width: 5%;
        font-size: 3em
    }

    .myText2 {
        color: #fff;
        width: 45%
    }

    .myDiv2 {
        width: 5%;
        font-size: 3em
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
