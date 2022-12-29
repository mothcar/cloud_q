<template>
  <q-page class="flex flex-center">
    <div class="max-width">

    <div class="row">
      <div class="col">
        <img
          alt="Quasar logo"
          src="~assets/quasar-logo-vertical.svg"
          style="width: 200px; height: 200px"
        >
      </div>
    </div>

    <div class="row text-center">
      <div class="col">
        <q-btn  class="flex-break" color="white" text-color="black" label="All User" @click="getAllUser"/>
      </div>
    </div>

    </div>
  </q-page>
</template>

<script>
// import axios from 'src/boot/axios.js';
import * as axios from 'axios';
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage',

  methods: {
    async getAllUser() {
      const url = 'https://port-0-m16-node-express-fao2flc8m4733.gksl2.cloudtype.app/'
      const res = await axios.get(url)
      console.log('get data : ', res)
    }
  }
})
</script>
