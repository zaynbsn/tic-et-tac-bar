<template>
  <div class="py-sm-5 bg-custom">
    <div class="container-fluid py-5 ">
    <div class="row p-5 text-light">
      <!-- About Title -->
        <h1 class="title text-start fw-bold ">
          Nous découvrir
        </h1>
        <p class="fs-6 textJustify">Le bar Tic & Tac est un bar à cocktails et bières situé au cœur de la place Jules Guesdes dans le septième arrondissement de Lyon. Nous aurons le plaisir de vous accueillir dans un lieu chaleureux disposant de deux salles aux ambiances complètement différentes.

      Le bar Tic & Tac propose une large gamme de cocktails classiques et originaux dont la plupart sont réalisés à partir de liqueurs maison. Un de ces cocktails, l’Élixir de jouvence, a été élaboré en exclusivité pour le bar Tic & Tac par un Meilleur Ouvrier de France barman.

      Le bar Tic & Tac, c’est également un important choix de bières artisanales et régionales. Que ce soit en pression ou en bouteille, vous trouverez sans aucun doute une bière qui saura satisfaire vos papilles.

      En cas de creux, Tic & Tac a également pensé à vous. Vous pourrez déguster de copieuses planches à partager élaborées à base de charcuteries, de fromages et de tartinades locaux.

      Dès les premiers beaux jours, vous pourrez également profiter de notre belle terrasse.</p>
    </div>
  </div>
  </div>
</template>
<script>
import { ref } from 'vue';

export default ({
  name:'About',
  setup() {
    
  },
})
</script>

<style scoped>
.textJustify{
    text-align: justify;
  text-justify: inter-word;
}
</style>
