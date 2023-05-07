<template>
  <div class="pt-5 bg-custom">
    <div class="container-fluid py-5 my-5">
    <div class="row  text-white">
        <div class="col-sm fs-4 textJustify">
            <p>
            Un afterwork, un anniversaire, un séminaire ou quelque chose à fêter ? Nous vous proposons de réserver sans frais un espace afin d’organiser votre évènement chez Tic & Tac Bar. Pour plus d’informations, n’hésitez pas à nous contacter (en précisant la date et l’heure souhaitées ainsi que le nombre d’invités).
            </p>
        </div>
        <div class="col-sm myEmail ">
            <a class="textYellowNoDeco fs-1 email" href="mailto:contact@tic-et-tac-bar.fr">contact@tic-et-tac-bar.fr</a>
                            
        </div>
    </div>
  </div>
  </div>
</template>

<script>
import { reactive, toRefs, watch } from 'vue'
    export default {
        name:'Contact',
        setup(){
        }
    }
</script>

<style scoped>
.textYellowNoDeco{
  color: #F6A424;
  text-decoration: none;
}
.textJustify{
    text-align: justify;
  text-justify: inter-word;
}
.email{
    margin-left: 15%;
}
</style>