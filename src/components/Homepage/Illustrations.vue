<template>
  <div class="d-flex flex-direction-columns justify-content-between align-items-center"  style="max-width: calc(100vw - 8px); overflow:hidden">
    <div class=" d-flex justify-content-center align-items-center" style="max-width: 30vw" >
      <img :src="Illustration1" alt="Illustration" style="max-height: 40vw" />
    </div>
    <div class=" d-flex justify-content-center align-items-center" style="max-width: 40vw" >
      <img :src="Illustration2" alt="Illustration" style="max-height: 40vw" />
    </div>
    <div class="d-flex justify-content-center align-items-center" style="max-width: 30vw" >
      <img :src="Illustration3" alt="Illustration" style="max-height: 40vw" />
    </div>
  </div>
  
  
</template>

<script>
import { reactive, toRefs } from 'vue'
import windowWidthMixin from '@/mixins/windowWidthMixin'

export default {
  name: 'Illustrations',
  mixins: [windowWidthMixin],
  setup() {
    let photos = reactive({
      Illustration1:require('@/assets/img/illustration1.png'),
      Illustration2:require('@/assets/img/illustration2.png'),
      Illustration3:require('@/assets/img/illustration3.png'),
    })

    return {...toRefs(photos)}
  }
}
</script>