<template>
	<div class="col-xs-12 col-sm-6">
    <p v-if='server==null'>Server Details are currently not updated</p>
    <p v-else> The server status of the server {{server.id}} is {{server.status}}</p>
  </div>
</template>

<script>
import {eventBus} from '../main'

export default {
  data () {
    return {
      server: null
    }
  },
  created () {
   
    eventBus.$on('changeServer', (server) => {
      this.server = server
       console.log('oaseee')
    })
  } 
}
</script>