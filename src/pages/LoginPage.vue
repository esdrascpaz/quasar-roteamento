<template>
  <div class="flex flex-center">
    <q-card class="my-card">
      <q-card-section>
        <q-input type="email" label="Email" />
        <q-input type="password" label="Senha" />
      </q-card-section>
      <q-card-section>
        <q-btn color="primary" icon="check" label="Entrar" />
      </q-card-section>
    </q-card>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage'
})
</script>
