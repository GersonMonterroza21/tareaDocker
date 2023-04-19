<template>

<q-toolbar-title absolute-center>

<h4><p align="center">Atrás va solo</p></h4>

</q-toolbar-title>
<div class="q-pa-md">
    <q-carousel
      swipeable
      animated
      v-model="slide"
      thumbnails
      infinite
      :autoplay="autoplay"
    >
      <q-carousel-slide :name="1" img-src="https://scontent.fsal3-1.fna.fbcdn.net/v/t1.15752-9/342169057_1640698446377320_6398848067392006312_n.jpg?_nc_cat=105&ccb=1-7&_nc_sid=ae9488&_nc_ohc=dJv8GunBICwAX93f2D8&_nc_ht=scontent.fsal3-1.fna&oh=03_AdQocEUM6SGujUYlQ12xArnEg2AvXE1bJFaWqLR4V2CaAg&oe=6466CA84" />

    </q-carousel>
  </div>
</template>
<script>
import { ref } from 'vue'


export default {
  setup () {
    return {
      slide: ref(1),
      autoplay: ref(true)
    }
  }
}
</script>
<style lang="">

</style>
