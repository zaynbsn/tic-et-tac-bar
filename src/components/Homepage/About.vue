<template>
  <div class="container my-5">
    <div class="row">
      <div class="col-sm-8 d-flex flex-column justify-content-center align-items-center">
        
        <Title label="Nous concernant" centered/>
        
        <div class="about-text mt-4" style="width: 75%;">
          <p v-for="(text, index) in texts" :key="index" class="fs-6 text-light qualityParag textJustify" >
            {{ text }}
          </p>
        </div>
      </div>

      <div class="col-sm-4 d-flex flex-column justify-content-center align-items-center">
          <img style="width: 80%;" :src="barmensImage" alt="About tic&tac barmens image">
      </div>

      <div v-if="isTouch" class="col-sm d-flex flex-column justify-content-center align-items-center my-3">
        <Button to="/about" label="En savoir plus" blank />   
      </div>
    </div>
  </div>
</template>

<script>
import { reactive, toRefs, ref } from 'vue'
import Title from '@/components/UI/Title.vue'
import windowWidthMixin from '@/mixins/windowWidthMixin'
import Button from '@/components/UI/Button.vue'

export default {
  name: 'About',
  components: { Title, Button },
  mixins: [windowWidthMixin],
  setup() {
    let photos = reactive({
      barmensImage:require('@/assets/img/barmens.jpg')
    })

    const texts = ref([
      'Le projet du bar Tic & Tac est né au détour d’une discussion en 2018. Il est le fruit de notre rencontre, Théo et Carl, sur les bancs de la fac.',
      'Littéralement indissociables, tout le monde nous appelait « Tic & Tac ». Nous avons donc naturellement choisi par la suite de nommer notre bar ainsi.',
      'Initialement prévu à Valence en Espagne, c’est bien à Lyon que nous avons finalement décidé d’ouvrir notre premier bar.',
      'Nous avons mis dans ce dernier les ingrédients résultant de tous les moments que nous avons partagés à deux comme nos nombreux voyages. C’est un bar à notre image, à celle de Tic & Tac.'
    ])

    
    return {...toRefs(photos), texts}
  }
}
</script>