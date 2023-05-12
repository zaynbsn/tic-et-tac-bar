<template>
  <div v-if="isWideScreen" class="container" style="margin-top: -12rem">
    <div class="row">
      <div class="col-sm-8 d-flex flex-column justify-content-center align-items-center">

        <Title label="Nous découvrir"/>

        <div class="discover-text" style="width: 75%;">
          <p v-for="(text, index) in texts" :key="index" class="fs-6 text-light qualityParag textJustify" >
              {{ text }}
          </p>
        </div>
      </div>

      <div class="col-sm-4 d-flex flex-column justify-content-center align-items-center">
          <img style="width: 80%;" :src="discoverImage" alt="Discover tic&tac bar image">
      </div>
    </div>
  </div>
</template>

<script>
import { reactive, toRefs, ref } from 'vue'
import Title from '../UI/Title.vue'
import windowWidthMixin from '@/mixins/windowWidthMixin'

export default {
  name: 'Discover',
  components: { Title },
  mixins: [windowWidthMixin],
  setup() {
    let photos = reactive({
      discoverImage:require('@/assets/img/discover.jpg')
    })

    const texts = ref([
      'Le bar Tic & Tac est un bar à cocktails et bières situé au cœur de la place Jules Guesdes dans le septième arrondissement de Lyon. Nous aurons le plaisir de vous accueillir dans un lieu chaleureux disposant de deux salles aux ambiances complètement différentes.',
      'Le bar Tic & Tac propose une large gamme de cocktails classiques et originaux dont la plupart sont réalisés à partir de liqueurs maison. Un de ces cocktails, l’Élixir de jouvence, a été élaboré en exclusivité pour le bar Tic & Tac par un Meilleur Ouvrier de France barman.',
      'Le bar Tic & Tac, c’est également un important choix de bières artisanales et régionales. Que ce soit en pression ou en bouteille, vous trouverez sans aucun doute une bière qui saura satisfaire vos papilles.',
      'En cas de creux, Tic & Tac a également pensé à vous. Vous pourrez déguster de copieuses planches à partager élaborées à base de charcuteries, de fromages et de tartinades locaux.',
      'Dès les premiers beaux jours, vous pourrez également profiter de notre belle terrasse.',
    ])

    
    return {...toRefs(photos), texts}
  }
}
</script>

<style lang="scss" scoped>
// .underline{
//     background: #ff8000;
//     height: 2px;
//     width: 4rem;
//     border-radius: 8px;
// }
// .discover-title h1{
//     font-size: 1.5rem;
//     font-weight: 600;
//     color: #fff;
//     margin-bottom: 1rem;
//     z-index: 3;
// }
.discover-text{
    margin-top: 2rem;
}
</style>