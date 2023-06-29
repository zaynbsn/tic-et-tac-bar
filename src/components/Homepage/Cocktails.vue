<template>

  <div class="container my-5">
    <Title label="Galerie de cocktails" :centered="isMobile" />

    <div class="row">
      <div v-for="(cocktail, index) in cocktails" :key="index" class="col-md-4 col-6 g-4">
        <div class="cardCarrou">
          <img :src="cocktail.src"  class="card-img-top" :alt="cocktail.alt">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { reactive, toRefs, ref } from 'vue'
import Title from '@/components/UI/Title.vue'
import windowWidthMixin from '@/mixins/windowWidthMixin'

export default {
  name: 'Cocktails',
  components: { Title },
  mixins: [windowWidthMixin],
  setup() {
    let photos = reactive({
      Cocktail1:require('@/assets/img/cocktail7.png'),
      Cocktail2:require('@/assets/img/cocktail2.png'),
      Cocktail3:require('@/assets/img/cocktail3.png'),
      Cocktail4:require('@/assets/img/cocktail4.png'),
      Cocktail5:require('@/assets/img/cocktail5.png'),
      Cocktail6:require('@/assets/img/cocktail6.png'),
    })

    const cocktails = ref([
      
      {
        src: photos.Cocktail2,
        alt: 'cocktail image'
      },
      {
        src: photos.Cocktail3,
        alt: 'cocktail image'
      },
      {
        src: photos.Cocktail4,
        alt: 'cocktail image'
      },
      {
        src: photos.Cocktail5,
        alt: 'cocktail image'
      },
      {
        src: photos.Cocktail6,
        alt: 'cocktail image'
      },
      {
        src: photos.Cocktail1,
        alt: 'cocktail image'
      },
    ])

    
    return {...toRefs(photos), cocktails}
  }
}
</script>