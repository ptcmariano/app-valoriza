<template>
  <div class="fullscreen bg-blue text-white text-center q-pa-md flex flex-center">
    <div>
      <div class="text-h2" style="opacity:.4">
        List User
      </div>
      <q-list bordered>
        <q-item
          v-for="item in listUser"
          :key="item.name"
        >{{item.name}}</q-item>
      </q-list>

      <q-btn
        class="q-mt-xl"
        color="white"
        text-color="blue"
        unelevated
        to="/index"
        label="Go Index"
        no-caps
      />
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'ListUserPage',
  setup() {
    return {
      listUser: [
        {name:"1"},
        {name:"2"},
        {name:"3"},
      ]
    }
  }
})
</script>
