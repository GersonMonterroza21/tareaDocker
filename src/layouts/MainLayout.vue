<template>
    <q-layout view="hhh LpR fFf" container style="height: 655px" class="shadow-2 rounded-borders">
      <q-header reveal class="bg-black glossy">
        <q-toolbar>
          <q-btn flat @click="drawerLeft = !drawerLeft" round dense icon="menu" />
          <q-toolbar-title>
            <p align="center">Diseño de sistemas 1</p></q-toolbar-title>
        </q-toolbar>
      </q-header>

      <q-footer elevated>
        <q-toolbar class="glossy">
          <q-toolbar-title>
            <p align="center">PREGUNTAS FRECUENTES | CONTACTANOS: pm20072@ues.edu.sv</p></q-toolbar-title>

        </q-toolbar>
      </q-footer>



      <q-drawer
        side="left"
        v-model="drawerLeft"
        bordered
        :width="200"
        :breakpoint="500"
        class="$q.dark.isActive ? 'bg-grey-9' : 'bg-grey-3'"
      >
        <q-scroll-area style="height: calc(100% - 150px); margin-top: 150px; border-right: 1px solid #ddd">
          <q-list padding>
            <q-item to="/miProyecto" clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="inbox" />
              </q-item-section>

              <q-item-section>
                miProyecto
              </q-item-section>
            </q-item>

            <q-item to="/miConocimiento" active clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="star" />
              </q-item-section>

              <q-item-section>
                miConocimiento
              </q-item-section>
            </q-item>
          </q-list>
        </q-scroll-area>

        <q-img class="absolute-top" src="https://cdn.quasar.dev/img/material.png" style="height: 150px">
          <div class="absolute-bottom bg-transparent">
            <q-avatar size="56px" class="q-mb-sm">
              <img src="https://scontent.fsal3-1.fna.fbcdn.net/v/t39.30808-6/257895481_1789625871222090_1559346117294232710_n.jpg?_nc_cat=110&ccb=1-7&_nc_sid=09cbfe&_nc_ohc=900tk-pUMY8AX9eB9YB&_nc_ht=scontent.fsal3-1.fna&oh=00_AfB85CFvJ9n7lVYFptl4Gaf35wIdtESiL4kK91BfiTpMRg&oe=6443AF96">
            </q-avatar>
            <div class="text-weight-bold">Gerson Alexis Pérez Monterroza</div>
            <div>PM20072</div>
          </div>
        </q-img>
      </q-drawer>

      <q-page-container>
        <router-view />
      </q-page-container>
    </q-layout>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      drawerLeft: ref(false),
      drawerRight: ref(true)
    }
  }
}
</script>
