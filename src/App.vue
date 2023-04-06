<template>
  <scedualAppointment/>
  <confirmedAppointment />
  <appointmentSummary/>
  <liveQueue />
  <markArrival />
  <arrivingSummary />
</template>

<script>
import scedualAppointment from './components/scedualAppointment.vue'
import confirmedAppointment from './components/confirmedAppointment.vue'
import appointmentSummary from './components/appointmentSummary.vue'
import liveQueue from './components/liveQueue.vue'
import markArrival from './components/markArrival.vue'
import arrivingSummary from './components/arrivingSummary.vue'



export default {
  name: 'App',
  components: {
    scedualAppointment,
    confirmedAppointment,
    appointmentSummary,
    liveQueue,
    markArrival,
    arrivingSummary,
  }
}
</script>

