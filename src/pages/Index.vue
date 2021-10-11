/* eslint-disable @typescript-eslint/no-unsafe-call */
<template>
  <q-page class="row items-center justify-evenly">

    <button @click="showDialog">showDialog</button>
  </q-page>

  <BaseDialog />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BaseDialog from 'src/components/BaseDialog.vue';

export default defineComponent({
  name: 'PageIndex',

  components: { BaseDialog },

  methods: {
    showDialog() {
      this.emitter.emit('showDialog', true);
    },
  },
});
</script>
