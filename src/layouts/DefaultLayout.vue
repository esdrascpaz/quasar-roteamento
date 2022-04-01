<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>Quasar App</q-toolbar-title>

        <div>
          <q-btn flat color="white" label="Nossos Produtos" @click="navigate('/')" />
          <q-btn flat color="white" label="Blog" @click="navigate('/blog')" />
          <q-btn flat color="white" label="Área do Cliente" @click="navigate('/login')" />
        </div>
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
    <q-footer reveal elevated bordered>
      <q-toolbar class="bg-purple text-white">
        <q-toolbar-title>
          <q-icon name="copyright" />
          {{ (new Date()).getFullYear() }}
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {

  },
  methods: {
    navigate (router = '') {
      this.$router.push(router)
    }
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {

      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
