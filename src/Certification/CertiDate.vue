<template>
  <div >
    <div >
      <q-date
        color="indigo-1"
        text-color="indigo-9"
        v-model="date"
        :events="events"
flat bordered
        style="width : 100%;
                border-radius: 10px"
      />


     </div>
      </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      date: ref('2019/02/01'),
      events: [ '2019/02/01', '2019/02/05', '2019/02/06', '2019/02/09', '2019/02/23' ],
      eventsFn (date) {
        const parts = date.split('/')
        return parts[ 2 ] % 2 === 0
      }
    }
  }
}
</script>

<style scoped>

</style>
