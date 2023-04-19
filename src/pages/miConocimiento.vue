<template>
    <div class="q-pa-md">
      <q-toolbar-title absolute-center>

        <h4><p align="center">Mi conocimiento</p></h4>

      </q-toolbar-title>
    <q-carousel
      swipeable
      animated
      v-model="slide"
      thumbnails
      infinite
      :autoplay="autoplay"
    >
      <q-carousel-slide :name="1" img-src="https://www.programaenlinea.net/wp-content/uploads/2020/08/php.png" />
      <q-carousel-slide :name="2" img-src="https://i.blogs.es/6e0b73/android-studio/1366_2000.png" />
      <q-carousel-slide :name="3" img-src="https://i.blogs.es/53044d/java/1366_521.jpg" />
      <q-carousel-slide :name="4" img-src="https://www.educative.io/v2api/editorpage/5295407815458816/image/4810048073629696" />
      <q-carousel-slide :name="4" img-src="https://www.icog.es/cursos/wp-content/uploads/2020/09/phyton.png" />
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
